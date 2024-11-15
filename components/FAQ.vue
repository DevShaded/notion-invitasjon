<script setup lang="ts">
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { MinusSmallIcon, PlusSmallIcon } from '@heroicons/vue/24/outline'

const faqs = [
  {
    question: "Hvem passer dette kurset for?",
    answer:
      "Kurset passer for alle som ønsker å forbedre sine organisasjonsferdigheter med Notion. Enten du er nybegynner eller har litt erfaring med Notion, vil du få nyttige tips og innsikt for å bruke verktøyet mer effektivt. Kurset dekker både grunnleggende og avanserte funksjoner, så det er relevant for både individuelle brukere og teammedlemmer.",
  },
  {
    question: "Trenger jeg noen forkunnskaper i Notion?",
    answer:
      "Nei, det er ikke nødvendig med forkunnskaper. Kurset starter med det grunnleggende, og vi vil gradvis bygge opp til mer avanserte funksjoner. Så lenge du har tilgang til Notion, er du klar til å delta!",
  },
  {
    question: "Må jeg laste ned programvare for å delta?",
    answer:
      "Notion er en skybasert plattform som du kan bruke i nettleseren, så det kreves ingen nedlasting. Det finnes også en desktop- og mobilapp for Notion, som kan være praktisk å ha, men det er ikke påkrevd for å delta i kurset.",
  },
  {
    question: "Hva slags funksjoner vil jeg lære om i kurset?",
    answer:
      "Du vil lære å bruke Notions brukergrensesnitt, opprette og organisere sider og undersider, og utnytte blokker til å lage innhold på en effektiv måte. I tillegg vil vi dekke hvordan du lager og bruker databaser, søker i innholdet, og samarbeider med andre ved å dele og kommentere. Kurset dekker også hvordan du publiserer sider på nett og får mest mulig ut av Notions søk- og filtreringsfunksjoner.",
  },
  {
    question: "Kan jeg stille spørsmål underveis i kurset?",
    answer:
      "Absolutt! Det vil være muligheter for å stille spørsmål gjennom hele kurset. Vi oppfordrer deltakere til å delta aktivt og spørre om alt de lurer på, slik at vi kan sikre at alle forstår materialet godt.",
  },
  {
    question: "Hvordan kan jeg bruke det jeg lærer i kurset på jobben eller i studiene?",
    answer:
      "Notion er et allsidig verktøy som kan brukes til prosjektstyring, oppgavelister, notat-taking, databehandling, og mye mer. Etter kurset vil du ha ferdigheter som kan hjelpe deg å organisere informasjon bedre, samarbeide effektivt med kollegaer eller medstudenter, og holde oversikt over viktige oppgaver og prosjekter.",
  },
  {
    question: "Får jeg kursmateriale eller opptak etter kurset?",
    answer:
      "Ja, alle deltakere vil få tilgang til kursmateriale, inkludert eksempler og maler som vi bruker under kurset. Hvis kurset blir tatt opp, vil du også få tilgang til opptaket, slik at du kan repetere innholdet senere.",
  },
  {
    question: "Hvor lenge varer kurset, og hvordan er det strukturert?",
    answer:
      "Kurset varer i 45 minutter og er designet for å gi en rask og effektiv gjennomgang av Notions viktigste funksjoner. Vi begynner med det grunnleggende, som navigasjon og oppretting av sider, og beveger oss raskt videre til databaser, søkefunksjoner, og samarbeid. Hver seksjon er kort og målrettet, slik at du får mest mulig ut av tiden.",
  }
]
</script>

<template>
  <section class="bg-white">
    <div class="mx-auto max-w-7xl px-6 py-24 sm:py-32 lg:px-8 lg:py-40">
      <div class="mx-auto max-w-4xl divide-y divide-gray-900/10">
        <h2 class="text-4xl italic tracking-tight text-gray-900 sm:text-5xl">Ofte stilte spørsmål</h2>
        <dl class="mt-10 space-y-6 divide-y divide-gray-900/10">
          <Disclosure as="div" v-for="faq in faqs" :key="faq.question" class="pt-6" v-slot="{ open }">
            <dt>
              <DisclosureButton class="flex w-full items-start justify-between text-left text-gray-900">
                <span class="text-base/7 font-semibold">{{ faq.question }}</span>
                <span class="ml-6 flex h-7 items-center">
                  <PlusSmallIcon v-if="!open" class="size-6" aria-hidden="true" />
                  <MinusSmallIcon v-else class="size-6" aria-hidden="true" />
                </span>
              </DisclosureButton>
            </dt>
            <DisclosurePanel as="dd" class="mt-2 pr-12">
              <p class="text-base/7 text-gray-600">{{ faq.answer }}</p>
            </DisclosurePanel>
          </Disclosure>
        </dl>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  font-family: 'Poppins', sans-serif;
}
</style>
