---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 7e5253951ec3c74850584aaac9818a6a7c8f2737
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622835"
---
# <span data-ttu-id="329db-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="329db-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="329db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="329db-102">SYNOPSIS</span></span>
<span data-ttu-id="329db-103">建立認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="329db-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="329db-104">句法</span><span class="sxs-lookup"><span data-stu-id="329db-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="329db-105">說明</span><span class="sxs-lookup"><span data-stu-id="329db-105">DESCRIPTION</span></span>
<span data-ttu-id="329db-106">**新的-AzCognitiveServicesAccount** Cmdlet 會建立具有指定類型和 SKU 的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="329db-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="329db-107">示例</span><span class="sxs-lookup"><span data-stu-id="329db-107">EXAMPLES</span></span>

### <span data-ttu-id="329db-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="329db-108">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
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

## <span data-ttu-id="329db-109">參數</span><span class="sxs-lookup"><span data-stu-id="329db-109">PARAMETERS</span></span>

### <span data-ttu-id="329db-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="329db-110">-CustomSubdomainName</span></span>
<span data-ttu-id="329db-111">認知服務帳戶子功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="329db-111">Cognitive Services Account Subdomain Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="329db-112">-DefaultProfile</span></span>
<span data-ttu-id="329db-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="329db-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="329db-114">-Force</span><span class="sxs-lookup"><span data-stu-id="329db-114">-Force</span></span>
<span data-ttu-id="329db-115">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="329db-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="329db-116">-位置</span><span class="sxs-lookup"><span data-stu-id="329db-116">-Location</span></span>
<span data-ttu-id="329db-117">指定要建立帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="329db-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="329db-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="329db-118">-Name</span></span>
<span data-ttu-id="329db-119">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="329db-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="329db-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="329db-120">-ResourceGroupName</span></span>
<span data-ttu-id="329db-121">指定要指派帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="329db-121">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="329db-122">資源群組必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="329db-122">The resource group must already exist.</span></span>

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

### <span data-ttu-id="329db-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="329db-123">-SkuName</span></span>
<span data-ttu-id="329db-124">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="329db-124">Specifies the SKU for the account.</span></span>
<span data-ttu-id="329db-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="329db-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="329db-126">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="329db-126">F0 (free tier)</span></span>
- <span data-ttu-id="329db-127">S0</span><span class="sxs-lookup"><span data-stu-id="329db-127">S0</span></span>
- <span data-ttu-id="329db-128">S1</span><span class="sxs-lookup"><span data-stu-id="329db-128">S1</span></span>
- <span data-ttu-id="329db-129">S2</span><span class="sxs-lookup"><span data-stu-id="329db-129">S2</span></span>
- <span data-ttu-id="329db-130">S3</span><span class="sxs-lookup"><span data-stu-id="329db-130">S3</span></span>
- <span data-ttu-id="329db-131">S4 如需詳細資訊，請參閱 [認知服務 api](https://www.microsoft.com/cognitive-services/en-us/apis)。</span><span class="sxs-lookup"><span data-stu-id="329db-131">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="329db-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="329db-132">-Tag</span></span>
<span data-ttu-id="329db-133">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="329db-133">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="329db-134">-類型</span><span class="sxs-lookup"><span data-stu-id="329db-134">-Type</span></span>
<span data-ttu-id="329db-135">指定要建立的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="329db-135">Specifies the type of account to create.</span></span> <span data-ttu-id="329db-136">使用 `Get-AzCognitiveServicesAccountType` Cmdlet 取得目前可接受的值。</span><span class="sxs-lookup"><span data-stu-id="329db-136">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="329db-137">-確認</span><span class="sxs-lookup"><span data-stu-id="329db-137">-Confirm</span></span>
<span data-ttu-id="329db-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="329db-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="329db-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="329db-139">-WhatIf</span></span>
<span data-ttu-id="329db-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="329db-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="329db-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="329db-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="329db-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329db-142">CommonParameters</span></span>
<span data-ttu-id="329db-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="329db-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="329db-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="329db-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329db-145">輸入</span><span class="sxs-lookup"><span data-stu-id="329db-145">INPUTS</span></span>

### <span data-ttu-id="329db-146">System.object</span><span class="sxs-lookup"><span data-stu-id="329db-146">System.String</span></span>

## <span data-ttu-id="329db-147">輸出</span><span class="sxs-lookup"><span data-stu-id="329db-147">OUTPUTS</span></span>

### <span data-ttu-id="329db-148">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="329db-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="329db-149">筆記</span><span class="sxs-lookup"><span data-stu-id="329db-149">NOTES</span></span>

## <span data-ttu-id="329db-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="329db-150">RELATED LINKS</span></span>

[<span data-ttu-id="329db-151">AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="329db-151">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="329db-152">移除-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="329db-152">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="329db-153">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="329db-153">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
