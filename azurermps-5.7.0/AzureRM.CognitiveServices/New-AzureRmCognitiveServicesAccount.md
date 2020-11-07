---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 1c1d4ad776ed3db2cb3b5adfb490902a7de12f42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623614"
---
# <span data-ttu-id="622b5-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="622b5-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="622b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="622b5-102">SYNOPSIS</span></span>
<span data-ttu-id="622b5-103">建立認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="622b5-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="622b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="622b5-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="622b5-105">說明</span><span class="sxs-lookup"><span data-stu-id="622b5-105">DESCRIPTION</span></span>
<span data-ttu-id="622b5-106">**新的-AzureRmCognitiveServicesAccount** Cmdlet 會建立具有指定類型和 SKU 的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="622b5-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="622b5-107">示例</span><span class="sxs-lookup"><span data-stu-id="622b5-107">EXAMPLES</span></span>

### <span data-ttu-id="622b5-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="622b5-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="622b5-109">參數</span><span class="sxs-lookup"><span data-stu-id="622b5-109">PARAMETERS</span></span>

### <span data-ttu-id="622b5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622b5-110">-DefaultProfile</span></span>
<span data-ttu-id="622b5-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="622b5-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622b5-112">-Force</span><span class="sxs-lookup"><span data-stu-id="622b5-112">-Force</span></span>
<span data-ttu-id="622b5-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="622b5-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622b5-114">-位置</span><span class="sxs-lookup"><span data-stu-id="622b5-114">-Location</span></span>
<span data-ttu-id="622b5-115">指定要建立帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="622b5-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="622b5-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="622b5-116">-Name</span></span>
<span data-ttu-id="622b5-117">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="622b5-117">Specifies the name for the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="622b5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="622b5-118">-ResourceGroupName</span></span>
<span data-ttu-id="622b5-119">指定要指派帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="622b5-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="622b5-120">資源群組必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="622b5-120">The resource group must already exist.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="622b5-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="622b5-121">-SkuName</span></span>
<span data-ttu-id="622b5-122">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="622b5-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="622b5-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="622b5-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="622b5-124">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="622b5-124">F0 (free tier)</span></span>
- <span data-ttu-id="622b5-125">S0</span><span class="sxs-lookup"><span data-stu-id="622b5-125">S0</span></span>
- <span data-ttu-id="622b5-126">S1</span><span class="sxs-lookup"><span data-stu-id="622b5-126">S1</span></span>
- <span data-ttu-id="622b5-127">S2</span><span class="sxs-lookup"><span data-stu-id="622b5-127">S2</span></span>
- <span data-ttu-id="622b5-128">S3</span><span class="sxs-lookup"><span data-stu-id="622b5-128">S3</span></span>
- <span data-ttu-id="622b5-129">喚醒</span><span class="sxs-lookup"><span data-stu-id="622b5-129">S4</span></span>

<span data-ttu-id="622b5-130">如需詳細資訊，請參閱 [認知服務 api](https://www.microsoft.com/cognitive-services/en-us/apis)。</span><span class="sxs-lookup"><span data-stu-id="622b5-130">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="622b5-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="622b5-131">-Tag</span></span>
<span data-ttu-id="622b5-132">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="622b5-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622b5-133">-類型</span><span class="sxs-lookup"><span data-stu-id="622b5-133">-Type</span></span>
<span data-ttu-id="622b5-134">指定要建立的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="622b5-134">Specifies the type of account to create.</span></span> <span data-ttu-id="622b5-135">此參數目前可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="622b5-135">Current acceptable values for this parameter are:</span></span>

- <span data-ttu-id="622b5-136">Bing. Autosuggest. v7</span><span class="sxs-lookup"><span data-stu-id="622b5-136">Bing.Autosuggest.v7</span></span>
- <span data-ttu-id="622b5-137">Bing. CustomSearch</span><span class="sxs-lookup"><span data-stu-id="622b5-137">Bing.CustomSearch</span></span>
- <span data-ttu-id="622b5-138">Bing. v7</span><span class="sxs-lookup"><span data-stu-id="622b5-138">Bing.Search.v7</span></span>
- <span data-ttu-id="622b5-139">Bing. 語音</span><span class="sxs-lookup"><span data-stu-id="622b5-139">Bing.Speech</span></span>
- <span data-ttu-id="622b5-140">Bing. 拼字檢查. v7</span><span class="sxs-lookup"><span data-stu-id="622b5-140">Bing.SpellCheck.v7</span></span>
- <span data-ttu-id="622b5-141">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="622b5-141">ComputerVision</span></span>
- <span data-ttu-id="622b5-142">ContentModerator</span><span class="sxs-lookup"><span data-stu-id="622b5-142">ContentModerator</span></span>
- <span data-ttu-id="622b5-143">CustomSpeech</span><span class="sxs-lookup"><span data-stu-id="622b5-143">CustomSpeech</span></span>
- <span data-ttu-id="622b5-144">CustomVision 聯想</span><span class="sxs-lookup"><span data-stu-id="622b5-144">CustomVision.Prediction</span></span>
- <span data-ttu-id="622b5-145">CustomVision 訓練</span><span class="sxs-lookup"><span data-stu-id="622b5-145">CustomVision.Training</span></span>
- <span data-ttu-id="622b5-146">表達</span><span class="sxs-lookup"><span data-stu-id="622b5-146">Emotion</span></span>
- <span data-ttu-id="622b5-147">還要</span><span class="sxs-lookup"><span data-stu-id="622b5-147">Face</span></span>
- <span data-ttu-id="622b5-148">LUIS</span><span class="sxs-lookup"><span data-stu-id="622b5-148">LUIS</span></span>
- <span data-ttu-id="622b5-149">QnAMaker</span><span class="sxs-lookup"><span data-stu-id="622b5-149">QnAMaker</span></span>
- <span data-ttu-id="622b5-150">SpeakerRecognition</span><span class="sxs-lookup"><span data-stu-id="622b5-150">SpeakerRecognition</span></span>
- <span data-ttu-id="622b5-151">SpeechTranslation</span><span class="sxs-lookup"><span data-stu-id="622b5-151">SpeechTranslation</span></span>
- <span data-ttu-id="622b5-152">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="622b5-152">TextAnalytics</span></span>
- <span data-ttu-id="622b5-153">TextTranslation</span><span class="sxs-lookup"><span data-stu-id="622b5-153">TextTranslation</span></span>
- <span data-ttu-id="622b5-154">WebLM</span><span class="sxs-lookup"><span data-stu-id="622b5-154">WebLM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="622b5-155">-確認</span><span class="sxs-lookup"><span data-stu-id="622b5-155">-Confirm</span></span>
<span data-ttu-id="622b5-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="622b5-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622b5-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="622b5-157">-WhatIf</span></span>
<span data-ttu-id="622b5-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="622b5-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="622b5-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="622b5-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622b5-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622b5-160">CommonParameters</span></span>
<span data-ttu-id="622b5-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="622b5-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622b5-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="622b5-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622b5-163">輸入</span><span class="sxs-lookup"><span data-stu-id="622b5-163">INPUTS</span></span>

### <span data-ttu-id="622b5-164">所有</span><span class="sxs-lookup"><span data-stu-id="622b5-164">None</span></span>
<span data-ttu-id="622b5-165">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="622b5-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="622b5-166">輸出</span><span class="sxs-lookup"><span data-stu-id="622b5-166">OUTPUTS</span></span>

### <span data-ttu-id="622b5-167">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="622b5-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="622b5-168">筆記</span><span class="sxs-lookup"><span data-stu-id="622b5-168">NOTES</span></span>

## <span data-ttu-id="622b5-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="622b5-169">RELATED LINKS</span></span>

[<span data-ttu-id="622b5-170">AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="622b5-170">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="622b5-171">移除-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="622b5-171">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="622b5-172">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="622b5-172">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
