---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: c7a4a34e3969f209bcd6fcaae46ed93cd316aba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447013"
---
# <span data-ttu-id="201a0-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="201a0-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="201a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="201a0-102">SYNOPSIS</span></span>
<span data-ttu-id="201a0-103">啟用或停用指定的智慧包。</span><span class="sxs-lookup"><span data-stu-id="201a0-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="201a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="201a0-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="201a0-105">說明</span><span class="sxs-lookup"><span data-stu-id="201a0-105">DESCRIPTION</span></span>
<span data-ttu-id="201a0-106">**AzureRmOperationalInsightsIntelligencePack** *Cmdlet 會啟用* 指定的智慧套件（如果啟用）設定為 $True，並在 [ *啟用* ] 設定為 [$False] 時停用。</span><span class="sxs-lookup"><span data-stu-id="201a0-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="201a0-107">示例</span><span class="sxs-lookup"><span data-stu-id="201a0-107">EXAMPLES</span></span>

### <span data-ttu-id="201a0-108">範例1：設定智慧套件</span><span class="sxs-lookup"><span data-stu-id="201a0-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="201a0-109">這個命令會啟用指定的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="201a0-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="201a0-110">參數</span><span class="sxs-lookup"><span data-stu-id="201a0-110">PARAMETERS</span></span>

### <span data-ttu-id="201a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201a0-111">-DefaultProfile</span></span>
<span data-ttu-id="201a0-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="201a0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="201a0-113">-啟用</span><span class="sxs-lookup"><span data-stu-id="201a0-113">-Enabled</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="201a0-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="201a0-114">-IntelligencePackName</span></span>
<span data-ttu-id="201a0-115">指定智慧套件名稱。</span><span class="sxs-lookup"><span data-stu-id="201a0-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="201a0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="201a0-116">-ResourceGroupName</span></span>
<span data-ttu-id="201a0-117">指定資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="201a0-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="201a0-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="201a0-118">-WorkspaceName</span></span>
<span data-ttu-id="201a0-119">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="201a0-119">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="201a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201a0-120">CommonParameters</span></span>
<span data-ttu-id="201a0-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="201a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201a0-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="201a0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201a0-123">輸入</span><span class="sxs-lookup"><span data-stu-id="201a0-123">INPUTS</span></span>

### <span data-ttu-id="201a0-124">所有</span><span class="sxs-lookup"><span data-stu-id="201a0-124">None</span></span>
<span data-ttu-id="201a0-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="201a0-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="201a0-126">輸出</span><span class="sxs-lookup"><span data-stu-id="201a0-126">OUTPUTS</span></span>

## <span data-ttu-id="201a0-127">筆記</span><span class="sxs-lookup"><span data-stu-id="201a0-127">NOTES</span></span>

## <span data-ttu-id="201a0-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="201a0-128">RELATED LINKS</span></span>

[<span data-ttu-id="201a0-129">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="201a0-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


