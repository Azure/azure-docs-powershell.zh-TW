---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: ce21b116ceb41bfdfb26008dd44c914f3198ab39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613825"
---
# <span data-ttu-id="7874f-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="7874f-101">New-AzAttestation</span></span>

## <span data-ttu-id="7874f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7874f-102">SYNOPSIS</span></span>
<span data-ttu-id="7874f-103">建立證明</span><span class="sxs-lookup"><span data-stu-id="7874f-103">Creates an attestation</span></span>

## <span data-ttu-id="7874f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7874f-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> [-AttestationPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7874f-105">說明</span><span class="sxs-lookup"><span data-stu-id="7874f-105">DESCRIPTION</span></span>
<span data-ttu-id="7874f-106">New-AzAttestation Cmdlet 會在指定的資源群組中建立證明。</span><span class="sxs-lookup"><span data-stu-id="7874f-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="7874f-107">示例</span><span class="sxs-lookup"><span data-stu-id="7874f-107">EXAMPLES</span></span>

### <span data-ttu-id="7874f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7874f-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```

<span data-ttu-id="7874f-109">在目前的訂閱中建立新的證明 "範例"，資源群組 "rg1"</span><span class="sxs-lookup"><span data-stu-id="7874f-109">Create a new Attestation "example" in current Subscription, Resource Group "rg1"</span></span>

## <span data-ttu-id="7874f-110">參數</span><span class="sxs-lookup"><span data-stu-id="7874f-110">PARAMETERS</span></span>

### <span data-ttu-id="7874f-111">-AttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="7874f-111">-AttestationPolicy</span></span>
<span data-ttu-id="7874f-112">指定所傳送的認證原則來建立證明。</span><span class="sxs-lookup"><span data-stu-id="7874f-112">Specifies the attestation policy passed in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7874f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7874f-113">-DefaultProfile</span></span>
<span data-ttu-id="7874f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7874f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7874f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="7874f-115">-Name</span></span>
<span data-ttu-id="7874f-116">指定要建立之實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="7874f-116">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="7874f-117">名稱可以是字母、數位或連字號的任何組合。</span><span class="sxs-lookup"><span data-stu-id="7874f-117">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="7874f-118">名稱必須以字母或數位開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="7874f-118">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="7874f-119">名稱必須是通用唯一的。</span><span class="sxs-lookup"><span data-stu-id="7874f-119">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7874f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7874f-120">-ResourceGroupName</span></span>
<span data-ttu-id="7874f-121">指定要在其中建立證明之現有資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7874f-121">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7874f-122">-確認</span><span class="sxs-lookup"><span data-stu-id="7874f-122">-Confirm</span></span>
<span data-ttu-id="7874f-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7874f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7874f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7874f-124">-WhatIf</span></span>
<span data-ttu-id="7874f-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7874f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7874f-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7874f-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7874f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7874f-127">CommonParameters</span></span>
<span data-ttu-id="7874f-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7874f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7874f-129">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7874f-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7874f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7874f-130">INPUTS</span></span>

### <span data-ttu-id="7874f-131">System.object</span><span class="sxs-lookup"><span data-stu-id="7874f-131">System.String</span></span>

## <span data-ttu-id="7874f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="7874f-132">OUTPUTS</span></span>

### <span data-ttu-id="7874f-133">PSAttestation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7874f-133">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="7874f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7874f-134">NOTES</span></span>

## <span data-ttu-id="7874f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="7874f-135">RELATED LINKS</span></span>
