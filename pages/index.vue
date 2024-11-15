<script setup lang="ts">
import { InformationCircleIcon } from '@heroicons/vue/20/solid'

useHead(() => ({
  title: 'Smartere med Notion',
  meta: [
    {
      name: 'description',
      content: 'Bli smarter med Notion! Lær hvordan du kan bruke Notion til å strukturere informasjon, samarbeide med andre, og skape effektive arbeidsflyter.',
    }
  ],
}))
</script>

<template>
  <div>
    <div class="fixed inset-x-0 bottom-14 z-20 flex items-center justify-center md:bottom-24">
      <div class="w-full max-w-2xl px-6 lg:px-10">
        <div class="-mx-1.5 w-[calc(100%+.625rem)] rounded-2xl border border-weaker bg-default/60 p-1.5 backdrop-blur-[1px]">
          <div class="relative overflow-hidden rounded-xl bg-default p-2 shadow-dialog forced-colors:outline">
              <div class="rounded-md bg-blue-50 p-4">
                <div class="flex">
                  <div class="shrink-0">
                    <InformationCircleIcon class="size-5 text-blue-400" aria-hidden="true" />
                  </div>
                  <div class="ml-3 flex-1 md:flex md:justify-between">
                    <p class="text-sm text-blue-700">Svar på vår spørreundersøkelse om Notion!</p>
                    <p class="mt-3 text-sm md:ml-6 md:mt-0">
                      <NuxtLink to="https://docs.google.com/forms/d/e/1FAIpQLSdy02Ln2nuOyoDxlyR2c5DmWDReeB_BTB_YWyMV9yLGtAk8NQ/viewform?usp=sf_link" target="_blank" class="whitespace-nowrap font-medium text-blue-700 hover:text-blue-600">
                        Ta undersøkelsen
                        <span aria-hidden="true"> &rarr;</span>
                      </NuxtLink>
                    </p>
                  </div>
                </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="relative font-sans text-default antialiased selection:bg-[#eff7ff]">
    <div class="relative mx-auto max-w-2xl px-6 pb-24 pt-8 text-base/[150%] sm:pb-32 lg:px-10">
      <div class="flex flex-col items-center justify-center">
        <NuxtImg
          class="size-18"
          src="/images/logo.svg"
          alt="Avatar"
          width="69"
          height="69"
        />
      </div>
      <header>
        <h1 class="mt-6 text-center font-serif text-4xl italic text-strong md:text-5xl">
          Smartere med Notion
        </h1>
      </header>

      <main>
        <p class="mt-4 sm:mt-6 md:mt-8 text-gray-600">
          Er du klar til å ta dine organisasjonsferdigheter til neste nivå? Bli med på vårt Notion-kurs og få en grundig innføring i hvordan du kan bruke Notion til å strukturere informasjon, samarbeide med andre, og skape effektive arbeidsflyter. I løpet av kurset vil vi dekke alt fra grunnleggende navigasjon og sideoppsett til avanserte funksjoner som databaser og søkefunksjoner.
        </p>

        <p class="mt-4 sm:mt-6 md:mt-8 text-gray-600">
          Vi starter med en gjennomgang av Notions grensesnitt og hvordan du setter opp arbeidsområder som passer dine behov. Du vil lære hvordan du lager nye sider og strukturerer innhold ved hjelp av blokker, samt hvordan du kan bruke undersider for å holde informasjon organisert. Deretter vil vi utforske hvordan databaser kan forenkle arbeidet ditt ved å tilby måter å lagre, sortere, og filtrere informasjon på, samtidig som du får innblikk i hvordan du kan bruke beregninger for å analysere data direkte i Notion.
        </p>

        <p class="mt-4 sm:mt-6 md:mt-8 text-gray-600">
          Kurset inkluderer også opplæring i hvordan du importerer informasjon, bruker Notions innebygde søkefunksjon for å finne det du trenger raskt, og hvordan du deler sider og samarbeider effektivt med andre. Vi ser på hvordan du kan bruke kommentarer for å gi tilbakemeldinger og opprette diskusjoner, og avslutter med en gjennomgang av hvordan du publiserer sider på nett for deling med et bredere publikum.
        </p>

        <p class="mt-4 sm:mt-6 md:mt-8 text-gray-600">
          Bli med og oppdag hvordan Notion kan forvandle din arbeidsflyt, enten du bruker det som et personlig produktivitetsverktøy eller som en plattform for teamarbeid.
        </p>

        <FAQ />
      </main>
    </div>

    <footer class="relative z-10 flex items-center justify-center gap-2 border-t border-default bg-default/80 px-6 py-4 text-xs text-weak">
      <p class="italic">
        © {{ new Date().getFullYear() }} Smartere med Notion. Alle rettigheter reservert.
      </p>
    </footer>
  </div>
</template>

<style scoped>
h1 {
  font-family: 'Instrument Serif', serif;
}

p {
  font-family: 'Inter', sans-serif;
}
</style>
