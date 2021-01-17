---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: efba6588697e34b371622eaa8a5f9a3c349d9ec0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449912"
---
# <span data-ttu-id="06e6b-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="06e6b-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="06e6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="06e6b-103">重新生成帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="06e6b-103">Regenerates an account key.</span></span>

## <span data-ttu-id="06e6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="06e6b-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06e6b-105">說明</span><span class="sxs-lookup"><span data-stu-id="06e6b-105">DESCRIPTION</span></span>
<span data-ttu-id="06e6b-106">**新的-AzCognitiveServicesAccountKey** Cmdlet 會為認知服務帳戶重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="06e6b-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="06e6b-107">示例</span><span class="sxs-lookup"><span data-stu-id="06e6b-107">EXAMPLES</span></span>

### <span data-ttu-id="06e6b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="06e6b-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="06e6b-109">參數</span><span class="sxs-lookup"><span data-stu-id="06e6b-109">PARAMETERS</span></span>

### <span data-ttu-id="06e6b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e6b-110">-DefaultProfile</span></span>
<span data-ttu-id="06e6b-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="06e6b-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06e6b-112">-Force</span><span class="sxs-lookup"><span data-stu-id="06e6b-112">-Force</span></span>
<span data-ttu-id="06e6b-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="06e6b-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06e6b-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="06e6b-114">-KeyName</span></span>
<span data-ttu-id="06e6b-115">指定要重新產生的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="06e6b-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="06e6b-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="06e6b-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06e6b-117">Key1</span><span class="sxs-lookup"><span data-stu-id="06e6b-117">Key1</span></span>
- <span data-ttu-id="06e6b-118">Key2</span><span class="sxs-lookup"><span data-stu-id="06e6b-118">Key2</span></span>

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

### <span data-ttu-id="06e6b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="06e6b-119">-Name</span></span>
<span data-ttu-id="06e6b-120">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="06e6b-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="06e6b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e6b-121">-ResourceGroupName</span></span>
<span data-ttu-id="06e6b-122">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06e6b-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="06e6b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="06e6b-123">-Confirm</span></span>
<span data-ttu-id="06e6b-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="06e6b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e6b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e6b-125">-WhatIf</span></span>
<span data-ttu-id="06e6b-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06e6b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06e6b-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06e6b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e6b-128">CommonParameters</span></span>
<span data-ttu-id="06e6b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06e6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e6b-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="06e6b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e6b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="06e6b-131">INPUTS</span></span>

### <span data-ttu-id="06e6b-132">System.object</span><span class="sxs-lookup"><span data-stu-id="06e6b-132">System.String</span></span>

### <span data-ttu-id="06e6b-133">CognitiveServices （名為模型）</span><span class="sxs-lookup"><span data-stu-id="06e6b-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="06e6b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="06e6b-134">OUTPUTS</span></span>

### <span data-ttu-id="06e6b-135">CognitiveServicesAccountKeys 中的 CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="06e6b-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="06e6b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="06e6b-136">NOTES</span></span>

## <span data-ttu-id="06e6b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="06e6b-137">RELATED LINKS</span></span>

[<span data-ttu-id="06e6b-138">AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="06e6b-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


