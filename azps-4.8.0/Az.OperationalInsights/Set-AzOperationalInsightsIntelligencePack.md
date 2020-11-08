---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126311"
---
# <span data-ttu-id="1874e-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="1874e-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="1874e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1874e-102">SYNOPSIS</span></span>
<span data-ttu-id="1874e-103">啟用或停用指定的智慧包。</span><span class="sxs-lookup"><span data-stu-id="1874e-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="1874e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1874e-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1874e-105">說明</span><span class="sxs-lookup"><span data-stu-id="1874e-105">DESCRIPTION</span></span>
<span data-ttu-id="1874e-106">**AzOperationalInsightsIntelligencePack** *Cmdlet 會啟用* 指定的智慧套件（如果啟用）設定為 $True，並在 [ *啟用* ] 設定為 [$False] 時停用。</span><span class="sxs-lookup"><span data-stu-id="1874e-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="1874e-107">示例</span><span class="sxs-lookup"><span data-stu-id="1874e-107">EXAMPLES</span></span>

### <span data-ttu-id="1874e-108">範例1：設定智慧套件</span><span class="sxs-lookup"><span data-stu-id="1874e-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="1874e-109">這個命令會啟用指定的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="1874e-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="1874e-110">參數</span><span class="sxs-lookup"><span data-stu-id="1874e-110">PARAMETERS</span></span>

### <span data-ttu-id="1874e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1874e-111">-DefaultProfile</span></span>
<span data-ttu-id="1874e-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1874e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1874e-113">-啟用</span><span class="sxs-lookup"><span data-stu-id="1874e-113">-Enabled</span></span>
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

### <span data-ttu-id="1874e-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="1874e-114">-IntelligencePackName</span></span>
<span data-ttu-id="1874e-115">指定智慧套件名稱。</span><span class="sxs-lookup"><span data-stu-id="1874e-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="1874e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1874e-116">-ResourceGroupName</span></span>
<span data-ttu-id="1874e-117">指定資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1874e-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="1874e-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1874e-118">-WorkspaceName</span></span>
<span data-ttu-id="1874e-119">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="1874e-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="1874e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1874e-120">CommonParameters</span></span>
<span data-ttu-id="1874e-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1874e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1874e-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1874e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1874e-123">輸入</span><span class="sxs-lookup"><span data-stu-id="1874e-123">INPUTS</span></span>

### <span data-ttu-id="1874e-124">System.object</span><span class="sxs-lookup"><span data-stu-id="1874e-124">System.String</span></span>

### <span data-ttu-id="1874e-125">System.object</span><span class="sxs-lookup"><span data-stu-id="1874e-125">System.Boolean</span></span>

## <span data-ttu-id="1874e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="1874e-126">OUTPUTS</span></span>

### <span data-ttu-id="1874e-127">PSIntelligencePack 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="1874e-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="1874e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="1874e-128">NOTES</span></span>

## <span data-ttu-id="1874e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1874e-129">RELATED LINKS</span></span>

[<span data-ttu-id="1874e-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1874e-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

