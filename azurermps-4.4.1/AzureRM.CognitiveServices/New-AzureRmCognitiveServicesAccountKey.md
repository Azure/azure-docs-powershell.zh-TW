---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 345e7c6365a66abde5f350f20f614d4d6c94b1b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456887"
---
# <span data-ttu-id="66dc0-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="66dc0-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="66dc0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="66dc0-103">重新生成帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="66dc0-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66dc0-104">句法</span><span class="sxs-lookup"><span data-stu-id="66dc0-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66dc0-105">說明</span><span class="sxs-lookup"><span data-stu-id="66dc0-105">DESCRIPTION</span></span>
<span data-ttu-id="66dc0-106">**新的-AzureRmCognitiveServicesAccountKey** Cmdlet 會為認知服務帳戶重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="66dc0-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="66dc0-107">示例</span><span class="sxs-lookup"><span data-stu-id="66dc0-107">EXAMPLES</span></span>

## <span data-ttu-id="66dc0-108">參數</span><span class="sxs-lookup"><span data-stu-id="66dc0-108">PARAMETERS</span></span>

### <span data-ttu-id="66dc0-109">-Force</span><span class="sxs-lookup"><span data-stu-id="66dc0-109">-Force</span></span>
<span data-ttu-id="66dc0-110">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="66dc0-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66dc0-111">-KeyName</span><span class="sxs-lookup"><span data-stu-id="66dc0-111">-KeyName</span></span>
<span data-ttu-id="66dc0-112">指定要重新產生的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="66dc0-112">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="66dc0-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="66dc0-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66dc0-114">Key1</span><span class="sxs-lookup"><span data-stu-id="66dc0-114">Key1</span></span>
- <span data-ttu-id="66dc0-115">Key2</span><span class="sxs-lookup"><span data-stu-id="66dc0-115">Key2</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66dc0-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="66dc0-116">-Name</span></span>
<span data-ttu-id="66dc0-117">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="66dc0-117">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="66dc0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66dc0-118">-ResourceGroupName</span></span>
<span data-ttu-id="66dc0-119">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66dc0-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="66dc0-120">-確認</span><span class="sxs-lookup"><span data-stu-id="66dc0-120">-Confirm</span></span>
<span data-ttu-id="66dc0-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66dc0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66dc0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66dc0-122">-WhatIf</span></span>
<span data-ttu-id="66dc0-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66dc0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66dc0-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66dc0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66dc0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66dc0-125">-DefaultProfile</span></span>
<span data-ttu-id="66dc0-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66dc0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66dc0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66dc0-127">CommonParameters</span></span>
<span data-ttu-id="66dc0-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66dc0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66dc0-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66dc0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66dc0-130">輸入</span><span class="sxs-lookup"><span data-stu-id="66dc0-130">INPUTS</span></span>

## <span data-ttu-id="66dc0-131">輸出</span><span class="sxs-lookup"><span data-stu-id="66dc0-131">OUTPUTS</span></span>

### <span data-ttu-id="66dc0-132">CognitiveServicesAccountKeys 中的 CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="66dc0-132">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="66dc0-133">筆記</span><span class="sxs-lookup"><span data-stu-id="66dc0-133">NOTES</span></span>

## <span data-ttu-id="66dc0-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="66dc0-134">RELATED LINKS</span></span>

[<span data-ttu-id="66dc0-135">AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="66dc0-135">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


