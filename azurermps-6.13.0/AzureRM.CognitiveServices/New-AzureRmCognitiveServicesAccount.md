---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41defe467244647f707bae16c653dfcbe99eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448465"
---
# <span data-ttu-id="2a319-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2a319-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="2a319-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a319-102">SYNOPSIS</span></span>
<span data-ttu-id="2a319-103">建立認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a319-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a319-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a319-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a319-105">說明</span><span class="sxs-lookup"><span data-stu-id="2a319-105">DESCRIPTION</span></span>
<span data-ttu-id="2a319-106">**新的-AzureRmCognitiveServicesAccount** Cmdlet 會建立具有指定類型和 SKU 的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a319-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="2a319-107">示例</span><span class="sxs-lookup"><span data-stu-id="2a319-107">EXAMPLES</span></span>

### <span data-ttu-id="2a319-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="2a319-108">1:</span></span>
```
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="2a319-109">參數</span><span class="sxs-lookup"><span data-stu-id="2a319-109">PARAMETERS</span></span>

### <span data-ttu-id="2a319-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a319-110">-DefaultProfile</span></span>
<span data-ttu-id="2a319-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2a319-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a319-112">-Force</span><span class="sxs-lookup"><span data-stu-id="2a319-112">-Force</span></span>
<span data-ttu-id="2a319-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2a319-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a319-114">-位置</span><span class="sxs-lookup"><span data-stu-id="2a319-114">-Location</span></span>
<span data-ttu-id="2a319-115">指定要建立帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="2a319-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a319-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a319-116">-Name</span></span>
<span data-ttu-id="2a319-117">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a319-117">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="2a319-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a319-118">-ResourceGroupName</span></span>
<span data-ttu-id="2a319-119">指定要指派帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a319-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="2a319-120">資源群組必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="2a319-120">The resource group must already exist.</span></span>

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

### <span data-ttu-id="2a319-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2a319-121">-SkuName</span></span>
<span data-ttu-id="2a319-122">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="2a319-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="2a319-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2a319-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2a319-124">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="2a319-124">F0 (free tier)</span></span>
- <span data-ttu-id="2a319-125">S0</span><span class="sxs-lookup"><span data-stu-id="2a319-125">S0</span></span>
- <span data-ttu-id="2a319-126">S1</span><span class="sxs-lookup"><span data-stu-id="2a319-126">S1</span></span>
- <span data-ttu-id="2a319-127">S2</span><span class="sxs-lookup"><span data-stu-id="2a319-127">S2</span></span>
- <span data-ttu-id="2a319-128">S3</span><span class="sxs-lookup"><span data-stu-id="2a319-128">S3</span></span>
- <span data-ttu-id="2a319-129">S4 如需詳細資訊，請參閱 [認知服務 api](https://www.microsoft.com/cognitive-services/en-us/apis)。</span><span class="sxs-lookup"><span data-stu-id="2a319-129">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a319-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a319-130">-Tag</span></span>
<span data-ttu-id="2a319-131">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="2a319-131">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a319-132">-類型</span><span class="sxs-lookup"><span data-stu-id="2a319-132">-Type</span></span>
<span data-ttu-id="2a319-133">指定要建立的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="2a319-133">Specifies the type of account to create.</span></span> <span data-ttu-id="2a319-134">使用 `Get-AzureRmCognitiveServicesAccountType` Cmdlet 取得目前可接受的值。</span><span class="sxs-lookup"><span data-stu-id="2a319-134">Use `Get-AzureRmCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a319-135">-確認</span><span class="sxs-lookup"><span data-stu-id="2a319-135">-Confirm</span></span>
<span data-ttu-id="2a319-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a319-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a319-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a319-137">-WhatIf</span></span>
<span data-ttu-id="2a319-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a319-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a319-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a319-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a319-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a319-140">CommonParameters</span></span>
<span data-ttu-id="2a319-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a319-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a319-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a319-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a319-143">輸入</span><span class="sxs-lookup"><span data-stu-id="2a319-143">INPUTS</span></span>

### <span data-ttu-id="2a319-144">System.object</span><span class="sxs-lookup"><span data-stu-id="2a319-144">System.String</span></span>

## <span data-ttu-id="2a319-145">輸出</span><span class="sxs-lookup"><span data-stu-id="2a319-145">OUTPUTS</span></span>

### <span data-ttu-id="2a319-146">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="2a319-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="2a319-147">筆記</span><span class="sxs-lookup"><span data-stu-id="2a319-147">NOTES</span></span>

## <span data-ttu-id="2a319-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a319-148">RELATED LINKS</span></span>

[<span data-ttu-id="2a319-149">AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2a319-149">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="2a319-150">移除-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2a319-150">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="2a319-151">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2a319-151">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
