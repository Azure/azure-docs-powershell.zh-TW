---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 266ee7c7dd8327a43de20faf0687e2f6a67ca6ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623650"
---
# <span data-ttu-id="b7d90-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="b7d90-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="b7d90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7d90-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d90-103">啟用或停用指定的智慧包。</span><span class="sxs-lookup"><span data-stu-id="b7d90-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7d90-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7d90-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7d90-105">說明</span><span class="sxs-lookup"><span data-stu-id="b7d90-105">DESCRIPTION</span></span>
<span data-ttu-id="b7d90-106">**AzureRmOperationalInsightsIntelligencePack** *Cmdlet 會啟用* 指定的智慧套件（如果啟用）設定為 $True，並在 [ *啟用* ] 設定為 [$False] 時停用。</span><span class="sxs-lookup"><span data-stu-id="b7d90-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="b7d90-107">示例</span><span class="sxs-lookup"><span data-stu-id="b7d90-107">EXAMPLES</span></span>

### <span data-ttu-id="b7d90-108">範例1：設定智慧套件</span><span class="sxs-lookup"><span data-stu-id="b7d90-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="b7d90-109">這個命令會啟用指定的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="b7d90-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="b7d90-110">參數</span><span class="sxs-lookup"><span data-stu-id="b7d90-110">PARAMETERS</span></span>

### <span data-ttu-id="b7d90-111">-啟用</span><span class="sxs-lookup"><span data-stu-id="b7d90-111">-Enabled</span></span>
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

### <span data-ttu-id="b7d90-112">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="b7d90-112">-IntelligencePackName</span></span>
<span data-ttu-id="b7d90-113">指定智慧套件名稱。</span><span class="sxs-lookup"><span data-stu-id="b7d90-113">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="b7d90-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7d90-114">-ResourceGroupName</span></span>
<span data-ttu-id="b7d90-115">指定資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b7d90-115">Specifies the resource group name</span></span>

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

### <span data-ttu-id="b7d90-116">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b7d90-116">-WorkspaceName</span></span>
<span data-ttu-id="b7d90-117">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7d90-117">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="b7d90-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d90-118">-DefaultProfile</span></span>
<span data-ttu-id="b7d90-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7d90-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7d90-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d90-120">CommonParameters</span></span>
<span data-ttu-id="b7d90-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7d90-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d90-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7d90-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d90-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b7d90-123">INPUTS</span></span>

## <span data-ttu-id="b7d90-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b7d90-124">OUTPUTS</span></span>

## <span data-ttu-id="b7d90-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b7d90-125">NOTES</span></span>

## <span data-ttu-id="b7d90-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7d90-126">RELATED LINKS</span></span>

[<span data-ttu-id="b7d90-127">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7d90-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


