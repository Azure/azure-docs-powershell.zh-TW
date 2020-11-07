---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 4701ae347f5a6ea8cd294a0ff75efa51f4d1370d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624616"
---
# <span data-ttu-id="bbaec-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="bbaec-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="bbaec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbaec-102">SYNOPSIS</span></span>
<span data-ttu-id="bbaec-103">重新生成帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="bbaec-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbaec-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbaec-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbaec-105">說明</span><span class="sxs-lookup"><span data-stu-id="bbaec-105">DESCRIPTION</span></span>
<span data-ttu-id="bbaec-106">**新的-AzureRmCognitiveServicesAccountKey** Cmdlet 會為認知服務帳戶重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="bbaec-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="bbaec-107">示例</span><span class="sxs-lookup"><span data-stu-id="bbaec-107">EXAMPLES</span></span>

### <span data-ttu-id="bbaec-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bbaec-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="bbaec-109">參數</span><span class="sxs-lookup"><span data-stu-id="bbaec-109">PARAMETERS</span></span>

### <span data-ttu-id="bbaec-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbaec-110">-DefaultProfile</span></span>
<span data-ttu-id="bbaec-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bbaec-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbaec-112">-Force</span><span class="sxs-lookup"><span data-stu-id="bbaec-112">-Force</span></span>
<span data-ttu-id="bbaec-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bbaec-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bbaec-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="bbaec-114">-KeyName</span></span>
<span data-ttu-id="bbaec-115">指定要重新產生的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="bbaec-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="bbaec-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bbaec-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bbaec-117">Key1</span><span class="sxs-lookup"><span data-stu-id="bbaec-117">Key1</span></span>
- <span data-ttu-id="bbaec-118">Key2</span><span class="sxs-lookup"><span data-stu-id="bbaec-118">Key2</span></span>

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

### <span data-ttu-id="bbaec-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="bbaec-119">-Name</span></span>
<span data-ttu-id="bbaec-120">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbaec-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="bbaec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbaec-121">-ResourceGroupName</span></span>
<span data-ttu-id="bbaec-122">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbaec-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="bbaec-123">-確認</span><span class="sxs-lookup"><span data-stu-id="bbaec-123">-Confirm</span></span>
<span data-ttu-id="bbaec-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bbaec-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbaec-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbaec-125">-WhatIf</span></span>
<span data-ttu-id="bbaec-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bbaec-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbaec-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bbaec-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbaec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbaec-128">CommonParameters</span></span>
<span data-ttu-id="bbaec-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbaec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbaec-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbaec-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbaec-131">輸入</span><span class="sxs-lookup"><span data-stu-id="bbaec-131">INPUTS</span></span>

### <span data-ttu-id="bbaec-132">System.object</span><span class="sxs-lookup"><span data-stu-id="bbaec-132">System.String</span></span>

### <span data-ttu-id="bbaec-133">CognitiveServices （名為模型）</span><span class="sxs-lookup"><span data-stu-id="bbaec-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="bbaec-134">輸出</span><span class="sxs-lookup"><span data-stu-id="bbaec-134">OUTPUTS</span></span>

### <span data-ttu-id="bbaec-135">CognitiveServicesAccountKeys 中的 CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="bbaec-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="bbaec-136">筆記</span><span class="sxs-lookup"><span data-stu-id="bbaec-136">NOTES</span></span>

## <span data-ttu-id="bbaec-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbaec-137">RELATED LINKS</span></span>

[<span data-ttu-id="bbaec-138">AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="bbaec-138">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


