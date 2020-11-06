---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2544531d9a988daaea314fc2088609df77b719b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622833"
---
# <span data-ttu-id="26f92-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="26f92-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="26f92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26f92-102">SYNOPSIS</span></span>
<span data-ttu-id="26f92-103">[修改帳戶]。</span><span class="sxs-lookup"><span data-stu-id="26f92-103">Modifies an account.</span></span>

## <span data-ttu-id="26f92-104">句法</span><span class="sxs-lookup"><span data-stu-id="26f92-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26f92-105">說明</span><span class="sxs-lookup"><span data-stu-id="26f92-105">DESCRIPTION</span></span>
<span data-ttu-id="26f92-106">**AzCognitiveServicesAccount** Cmdlet 會修改指定的認知服務帳戶的 SKU 或標記。</span><span class="sxs-lookup"><span data-stu-id="26f92-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="26f92-107">示例</span><span class="sxs-lookup"><span data-stu-id="26f92-107">EXAMPLES</span></span>

### <span data-ttu-id="26f92-108">範例1</span><span class="sxs-lookup"><span data-stu-id="26f92-108">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="26f92-109">參數</span><span class="sxs-lookup"><span data-stu-id="26f92-109">PARAMETERS</span></span>

### <span data-ttu-id="26f92-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f92-110">-DefaultProfile</span></span>
<span data-ttu-id="26f92-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="26f92-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f92-112">-Force</span><span class="sxs-lookup"><span data-stu-id="26f92-112">-Force</span></span>
<span data-ttu-id="26f92-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="26f92-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f92-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="26f92-114">-Name</span></span>
<span data-ttu-id="26f92-115">指定要修改的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="26f92-115">Specifies the name of the account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f92-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f92-116">-ResourceGroupName</span></span>
<span data-ttu-id="26f92-117">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26f92-117">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f92-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="26f92-118">-SkuName</span></span>
<span data-ttu-id="26f92-119">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="26f92-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="26f92-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="26f92-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26f92-121">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="26f92-121">F0 (free tier)</span></span>
- <span data-ttu-id="26f92-122">S0</span><span class="sxs-lookup"><span data-stu-id="26f92-122">S0</span></span>
- <span data-ttu-id="26f92-123">S1</span><span class="sxs-lookup"><span data-stu-id="26f92-123">S1</span></span>
- <span data-ttu-id="26f92-124">S2</span><span class="sxs-lookup"><span data-stu-id="26f92-124">S2</span></span>
- <span data-ttu-id="26f92-125">S3</span><span class="sxs-lookup"><span data-stu-id="26f92-125">S3</span></span>
- <span data-ttu-id="26f92-126">喚醒</span><span class="sxs-lookup"><span data-stu-id="26f92-126">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f92-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="26f92-127">-Tag</span></span>
<span data-ttu-id="26f92-128">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="26f92-128">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f92-129">-確認</span><span class="sxs-lookup"><span data-stu-id="26f92-129">-Confirm</span></span>
<span data-ttu-id="26f92-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26f92-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f92-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f92-131">-WhatIf</span></span>
<span data-ttu-id="26f92-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26f92-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26f92-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26f92-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f92-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f92-134">CommonParameters</span></span>
<span data-ttu-id="26f92-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26f92-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f92-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26f92-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f92-137">輸入</span><span class="sxs-lookup"><span data-stu-id="26f92-137">INPUTS</span></span>

### <span data-ttu-id="26f92-138">System.object</span><span class="sxs-lookup"><span data-stu-id="26f92-138">System.String</span></span>

### <span data-ttu-id="26f92-139">[System.object]。 Hashtable []</span><span class="sxs-lookup"><span data-stu-id="26f92-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="26f92-140">輸出</span><span class="sxs-lookup"><span data-stu-id="26f92-140">OUTPUTS</span></span>

### <span data-ttu-id="26f92-141">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="26f92-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="26f92-142">筆記</span><span class="sxs-lookup"><span data-stu-id="26f92-142">NOTES</span></span>

## <span data-ttu-id="26f92-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="26f92-143">RELATED LINKS</span></span>

[<span data-ttu-id="26f92-144">AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="26f92-144">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="26f92-145">新-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="26f92-145">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="26f92-146">移除-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="26f92-146">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
