---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 22e4f7e115016930e3745e5ce317a3deaa84ad71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909218"
---
# <span data-ttu-id="6ccad-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="6ccad-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="6ccad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6ccad-102">SYNOPSIS</span></span>
<span data-ttu-id="6ccad-103">重新產生帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="6ccad-103">Regenerates an account key.</span></span>

## <span data-ttu-id="6ccad-104">語法</span><span class="sxs-lookup"><span data-stu-id="6ccad-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ccad-105">描述</span><span class="sxs-lookup"><span data-stu-id="6ccad-105">DESCRIPTION</span></span>
<span data-ttu-id="6ccad-106">**New-AzCognitiveServicesAccountKey** Cmdlet 會重新產生認知服務帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="6ccad-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="6ccad-107">例子</span><span class="sxs-lookup"><span data-stu-id="6ccad-107">EXAMPLES</span></span>

### <span data-ttu-id="6ccad-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6ccad-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="6ccad-109">參數</span><span class="sxs-lookup"><span data-stu-id="6ccad-109">PARAMETERS</span></span>

### <span data-ttu-id="6ccad-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ccad-110">-DefaultProfile</span></span>
<span data-ttu-id="6ccad-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6ccad-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ccad-112">-強制</span><span class="sxs-lookup"><span data-stu-id="6ccad-112">-Force</span></span>
<span data-ttu-id="6ccad-113">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6ccad-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6ccad-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6ccad-114">-KeyName</span></span>
<span data-ttu-id="6ccad-115">指定要重新產生之金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ccad-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="6ccad-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6ccad-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6ccad-117">Key1</span><span class="sxs-lookup"><span data-stu-id="6ccad-117">Key1</span></span>
- <span data-ttu-id="6ccad-118">Key2</span><span class="sxs-lookup"><span data-stu-id="6ccad-118">Key2</span></span>

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

### <span data-ttu-id="6ccad-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ccad-119">-Name</span></span>
<span data-ttu-id="6ccad-120">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ccad-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="6ccad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ccad-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ccad-122">指定帳戶指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6ccad-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="6ccad-123">-確認</span><span class="sxs-lookup"><span data-stu-id="6ccad-123">-Confirm</span></span>
<span data-ttu-id="6ccad-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6ccad-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ccad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ccad-125">-WhatIf</span></span>
<span data-ttu-id="6ccad-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ccad-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ccad-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ccad-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ccad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ccad-128">CommonParameters</span></span>
<span data-ttu-id="6ccad-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6ccad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ccad-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ccad-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ccad-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6ccad-131">INPUTS</span></span>

### <span data-ttu-id="6ccad-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6ccad-132">System.String</span></span>

### <span data-ttu-id="6ccad-133">Microsoft.Azure.management.CognitiveServices.models.KeyName</span><span class="sxs-lookup"><span data-stu-id="6ccad-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="6ccad-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6ccad-134">OUTPUTS</span></span>

### <span data-ttu-id="6ccad-135">Microsoft.Azure.management.CognitiveServices.models.CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6ccad-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="6ccad-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6ccad-136">NOTES</span></span>

## <span data-ttu-id="6ccad-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ccad-137">RELATED LINKS</span></span>

[<span data-ttu-id="6ccad-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="6ccad-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


