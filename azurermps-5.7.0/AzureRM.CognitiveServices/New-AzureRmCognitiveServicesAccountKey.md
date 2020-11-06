---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 1c3ebaf3e95c1094b02b73505e471d13015721d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446412"
---
# <span data-ttu-id="88b05-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="88b05-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="88b05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88b05-102">SYNOPSIS</span></span>
<span data-ttu-id="88b05-103">重新生成帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="88b05-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88b05-104">句法</span><span class="sxs-lookup"><span data-stu-id="88b05-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88b05-105">說明</span><span class="sxs-lookup"><span data-stu-id="88b05-105">DESCRIPTION</span></span>
<span data-ttu-id="88b05-106">**新的-AzureRmCognitiveServicesAccountKey** Cmdlet 會為認知服務帳戶重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="88b05-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="88b05-107">示例</span><span class="sxs-lookup"><span data-stu-id="88b05-107">EXAMPLES</span></span>

## <span data-ttu-id="88b05-108">參數</span><span class="sxs-lookup"><span data-stu-id="88b05-108">PARAMETERS</span></span>

### <span data-ttu-id="88b05-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b05-109">-DefaultProfile</span></span>
<span data-ttu-id="88b05-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="88b05-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88b05-111">-Force</span><span class="sxs-lookup"><span data-stu-id="88b05-111">-Force</span></span>
<span data-ttu-id="88b05-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="88b05-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88b05-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="88b05-113">-KeyName</span></span>
<span data-ttu-id="88b05-114">指定要重新產生的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="88b05-114">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="88b05-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="88b05-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88b05-116">Key1</span><span class="sxs-lookup"><span data-stu-id="88b05-116">Key1</span></span>
- <span data-ttu-id="88b05-117">Key2</span><span class="sxs-lookup"><span data-stu-id="88b05-117">Key2</span></span>

```yaml
Type: KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88b05-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="88b05-118">-Name</span></span>
<span data-ttu-id="88b05-119">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="88b05-119">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="88b05-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b05-120">-ResourceGroupName</span></span>
<span data-ttu-id="88b05-121">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88b05-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="88b05-122">-確認</span><span class="sxs-lookup"><span data-stu-id="88b05-122">-Confirm</span></span>
<span data-ttu-id="88b05-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88b05-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88b05-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88b05-124">-WhatIf</span></span>
<span data-ttu-id="88b05-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88b05-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88b05-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88b05-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88b05-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b05-127">CommonParameters</span></span>
<span data-ttu-id="88b05-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88b05-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b05-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88b05-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b05-130">輸入</span><span class="sxs-lookup"><span data-stu-id="88b05-130">INPUTS</span></span>

### <span data-ttu-id="88b05-131">所有</span><span class="sxs-lookup"><span data-stu-id="88b05-131">None</span></span>
<span data-ttu-id="88b05-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="88b05-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88b05-133">輸出</span><span class="sxs-lookup"><span data-stu-id="88b05-133">OUTPUTS</span></span>

### <span data-ttu-id="88b05-134">CognitiveServicesAccountKeys 中的 CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="88b05-134">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="88b05-135">筆記</span><span class="sxs-lookup"><span data-stu-id="88b05-135">NOTES</span></span>

## <span data-ttu-id="88b05-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="88b05-136">RELATED LINKS</span></span>

[<span data-ttu-id="88b05-137">AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="88b05-137">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


