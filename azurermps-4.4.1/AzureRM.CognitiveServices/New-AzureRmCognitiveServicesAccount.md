---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 449b10f851dbd4e2f2e804bab0772543d512c0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456888"
---
# <span data-ttu-id="e37e2-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e37e2-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="e37e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e37e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e37e2-103">建立認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="e37e2-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e37e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="e37e2-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e37e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="e37e2-105">DESCRIPTION</span></span>
<span data-ttu-id="e37e2-106">**新的-AzureRmCognitiveServicesAccount** Cmdlet 會建立具有指定類型和 SKU 的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="e37e2-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="e37e2-107">示例</span><span class="sxs-lookup"><span data-stu-id="e37e2-107">EXAMPLES</span></span>

### <span data-ttu-id="e37e2-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="e37e2-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="e37e2-109">參數</span><span class="sxs-lookup"><span data-stu-id="e37e2-109">PARAMETERS</span></span>

### <span data-ttu-id="e37e2-110">-Force</span><span class="sxs-lookup"><span data-stu-id="e37e2-110">-Force</span></span>
<span data-ttu-id="e37e2-111">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e37e2-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e37e2-112">-位置</span><span class="sxs-lookup"><span data-stu-id="e37e2-112">-Location</span></span>
<span data-ttu-id="e37e2-113">指定要建立帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="e37e2-113">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="e37e2-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="e37e2-114">-Name</span></span>
<span data-ttu-id="e37e2-115">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e37e2-115">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="e37e2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e37e2-116">-ResourceGroupName</span></span>
<span data-ttu-id="e37e2-117">指定要指派帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e37e2-117">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="e37e2-118">資源群組必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="e37e2-118">The resource group must already exist.</span></span>

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

### <span data-ttu-id="e37e2-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e37e2-119">-SkuName</span></span>
<span data-ttu-id="e37e2-120">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="e37e2-120">Specifies the SKU for the account.</span></span>
<span data-ttu-id="e37e2-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e37e2-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e37e2-122">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="e37e2-122">F0 (free tier)</span></span>
- <span data-ttu-id="e37e2-123">S0</span><span class="sxs-lookup"><span data-stu-id="e37e2-123">S0</span></span>
- <span data-ttu-id="e37e2-124">S1</span><span class="sxs-lookup"><span data-stu-id="e37e2-124">S1</span></span>
- <span data-ttu-id="e37e2-125">S2</span><span class="sxs-lookup"><span data-stu-id="e37e2-125">S2</span></span>
- <span data-ttu-id="e37e2-126">S3</span><span class="sxs-lookup"><span data-stu-id="e37e2-126">S3</span></span>
- <span data-ttu-id="e37e2-127">喚醒</span><span class="sxs-lookup"><span data-stu-id="e37e2-127">S4</span></span>

<span data-ttu-id="e37e2-128">如需詳細資訊，請參閱 [認知服務 api](https://www.microsoft.com/cognitive-services/en-us/apis)。</span><span class="sxs-lookup"><span data-stu-id="e37e2-128">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="e37e2-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="e37e2-129">-Tag</span></span>
<span data-ttu-id="e37e2-130">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="e37e2-130">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="e37e2-131">-類型</span><span class="sxs-lookup"><span data-stu-id="e37e2-131">-Type</span></span>
<span data-ttu-id="e37e2-132">指定要建立的帳戶類型。此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e37e2-132">Specifies the type of account to create.The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e37e2-133">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="e37e2-133">ComputerVision</span></span>
- <span data-ttu-id="e37e2-134">表達</span><span class="sxs-lookup"><span data-stu-id="e37e2-134">Emotion</span></span>
- <span data-ttu-id="e37e2-135">還要</span><span class="sxs-lookup"><span data-stu-id="e37e2-135">Face</span></span>
- <span data-ttu-id="e37e2-136">LUIS</span><span class="sxs-lookup"><span data-stu-id="e37e2-136">LUIS</span></span>
- <span data-ttu-id="e37e2-137">提出</span><span class="sxs-lookup"><span data-stu-id="e37e2-137">Recommendations</span></span>
- <span data-ttu-id="e37e2-138">留言</span><span class="sxs-lookup"><span data-stu-id="e37e2-138">Speech</span></span>
- <span data-ttu-id="e37e2-139">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="e37e2-139">TextAnalytics</span></span>
- <span data-ttu-id="e37e2-140">WebLM</span><span class="sxs-lookup"><span data-stu-id="e37e2-140">WebLM</span></span>

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

### <span data-ttu-id="e37e2-141">-確認</span><span class="sxs-lookup"><span data-stu-id="e37e2-141">-Confirm</span></span>
<span data-ttu-id="e37e2-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e37e2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e37e2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e37e2-143">-WhatIf</span></span>
<span data-ttu-id="e37e2-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e37e2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e37e2-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e37e2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e37e2-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e37e2-146">-DefaultProfile</span></span>
<span data-ttu-id="e37e2-147">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e37e2-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e37e2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e37e2-148">CommonParameters</span></span>
<span data-ttu-id="e37e2-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e37e2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e37e2-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e37e2-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e37e2-151">輸入</span><span class="sxs-lookup"><span data-stu-id="e37e2-151">INPUTS</span></span>

## <span data-ttu-id="e37e2-152">輸出</span><span class="sxs-lookup"><span data-stu-id="e37e2-152">OUTPUTS</span></span>

### <span data-ttu-id="e37e2-153">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="e37e2-153">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="e37e2-154">筆記</span><span class="sxs-lookup"><span data-stu-id="e37e2-154">NOTES</span></span>

## <span data-ttu-id="e37e2-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="e37e2-155">RELATED LINKS</span></span>

[<span data-ttu-id="e37e2-156">AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e37e2-156">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="e37e2-157">移除-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e37e2-157">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="e37e2-158">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e37e2-158">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
