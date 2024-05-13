<script setup lang="ts">
import {
  Crown,
  Vegan,
  Ghost,
  Puzzle,
  Squirrel,
  Cookie,
  Drama,
} from "lucide-vue-next";

interface sponsorsProps {
  icon: string;
  name: string;
}

const sponsors: sponsorsProps[] = [
  {
    icon: "crown",
    name: "Acmebrand",
  },
  {
    icon: "vegan",
    name: "Acmelogo",
  },
  {
    icon: "ghost",
    name: "Acmesponsor",
  },
  {
    icon: "puzzle",
    name: "Acmeipsum",
  },
  {
    icon: "squirrel",
    name: "Acme",
  },
  {
    icon: "cookie",
    name: "Accmee",
  },
  {
    icon: "drama",
    name: "Acmetech",
  },
];

const iconMap: Record<
  string,
  | typeof Crown
  | typeof Vegan
  | typeof Ghost
  | typeof Puzzle
  | typeof Squirrel
  | typeof Cookie
  | typeof Drama
> = {
  crown: Crown,
  vegan: Vegan,
  ghost: Ghost,
  puzzle: Puzzle,
  squirrel: Squirrel,
  cookie: Cookie,
  drama: Drama,
};
</script>

<template>
  <section class="container pb-24 sm:pb-32">
    <h2 class="text-lg md:text-xl text-center mb-6">Our Platinum Sponsors</h2>

    <div class="mx-auto flex flex-row justify-center flex-wrap gap-8">
      <div
        v-for="{ icon, name } in sponsors"
        :key="name"
      >
        <div class="flex items-center text-xl md:text-2xl font-medium">
          <component
            :is="iconMap[icon]"
            class="mr-2"
            stroke-width="3"
          />
          {{ name }}
        </div>
      </div>
    </div>
  </section>
</template>
