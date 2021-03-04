---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: ee65492adc8c2756a2d19871e4c673668d471c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911549"
---
# <span data-ttu-id="56ed0-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="56ed0-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="56ed0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="56ed0-103">啟用或停用指定的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="56ed0-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="56ed0-104">語法</span><span class="sxs-lookup"><span data-stu-id="56ed0-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56ed0-105">描述</span><span class="sxs-lookup"><span data-stu-id="56ed0-105">DESCRIPTION</span></span>
<span data-ttu-id="56ed0-106">**Set-AzOperationalInsightsIntelligencePack** Cmdlet 會啟用指定的智慧套件 ，如果 *Enabled* 設定為 $True，且如果 *Enabled* 設為 $False，則停用它。</span><span class="sxs-lookup"><span data-stu-id="56ed0-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="56ed0-107">例子</span><span class="sxs-lookup"><span data-stu-id="56ed0-107">EXAMPLES</span></span>

### <span data-ttu-id="56ed0-108">範例 1：設定智慧套件</span><span class="sxs-lookup"><span data-stu-id="56ed0-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="56ed0-109">此命令會啟用指定的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="56ed0-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="56ed0-110">參數</span><span class="sxs-lookup"><span data-stu-id="56ed0-110">PARAMETERS</span></span>

### <span data-ttu-id="56ed0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ed0-111">-DefaultProfile</span></span>
<span data-ttu-id="56ed0-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="56ed0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56ed0-113">-已啟用</span><span class="sxs-lookup"><span data-stu-id="56ed0-113">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56ed0-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="56ed0-114">-IntelligencePackName</span></span>
<span data-ttu-id="56ed0-115">指定智慧套件名稱。</span><span class="sxs-lookup"><span data-stu-id="56ed0-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56ed0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ed0-116">-ResourceGroupName</span></span>
<span data-ttu-id="56ed0-117">指定資源組名</span><span class="sxs-lookup"><span data-stu-id="56ed0-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="56ed0-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="56ed0-118">-WorkspaceName</span></span>
<span data-ttu-id="56ed0-119">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="56ed0-119">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56ed0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ed0-120">CommonParameters</span></span>
<span data-ttu-id="56ed0-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56ed0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ed0-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="56ed0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ed0-123">輸入</span><span class="sxs-lookup"><span data-stu-id="56ed0-123">INPUTS</span></span>

### <span data-ttu-id="56ed0-124">System.String</span><span class="sxs-lookup"><span data-stu-id="56ed0-124">System.String</span></span>

### <span data-ttu-id="56ed0-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="56ed0-125">System.Boolean</span></span>

## <span data-ttu-id="56ed0-126">輸出</span><span class="sxs-lookup"><span data-stu-id="56ed0-126">OUTPUTS</span></span>

### <span data-ttu-id="56ed0-127">Microsoft.Azure.Commands.OperationalInsights.models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="56ed0-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="56ed0-128">筆記</span><span class="sxs-lookup"><span data-stu-id="56ed0-128">NOTES</span></span>

## <span data-ttu-id="56ed0-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="56ed0-129">RELATED LINKS</span></span>

[<span data-ttu-id="56ed0-130">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="56ed0-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


