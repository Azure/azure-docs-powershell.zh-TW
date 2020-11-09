---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285841"
---
# <span data-ttu-id="c5535-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c5535-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="c5535-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5535-102">SYNOPSIS</span></span>
<span data-ttu-id="c5535-103">取得連接至工作區之管理群組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c5535-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="c5535-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5535-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5535-105">說明</span><span class="sxs-lookup"><span data-stu-id="c5535-105">DESCRIPTION</span></span>
<span data-ttu-id="c5535-106">**AzOperationalInsightsWorkspaceManagementGroup** Cmdlet 會列出已連接至工作區的管理群組。</span><span class="sxs-lookup"><span data-stu-id="c5535-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="c5535-107">示例</span><span class="sxs-lookup"><span data-stu-id="c5535-107">EXAMPLES</span></span>

### <span data-ttu-id="c5535-108">範例1：依工作區名稱取得管理群組</span><span class="sxs-lookup"><span data-stu-id="c5535-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="c5535-109">這個命令會取得名為 ContosoResourceGroup 之資源群組中名為 MyWorkspace 之工作區的管理群組。</span><span class="sxs-lookup"><span data-stu-id="c5535-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c5535-110">範例2：使用管線取得管理群組</span><span class="sxs-lookup"><span data-stu-id="c5535-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="c5535-111">這個命令會使用 Get-AzOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後將工作區傳送至目前的 Cmdlet，以取得該工作區的管理群組。</span><span class="sxs-lookup"><span data-stu-id="c5535-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="c5535-112">參數</span><span class="sxs-lookup"><span data-stu-id="c5535-112">PARAMETERS</span></span>

### <span data-ttu-id="c5535-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5535-113">-DefaultProfile</span></span>
<span data-ttu-id="c5535-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c5535-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5535-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5535-115">-Name</span></span>
<span data-ttu-id="c5535-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="c5535-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5535-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5535-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5535-118">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5535-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="c5535-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5535-119">CommonParameters</span></span>
<span data-ttu-id="c5535-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5535-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5535-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5535-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5535-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c5535-122">INPUTS</span></span>

### <span data-ttu-id="c5535-123">System.object</span><span class="sxs-lookup"><span data-stu-id="c5535-123">System.String</span></span>

## <span data-ttu-id="c5535-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c5535-124">OUTPUTS</span></span>

### <span data-ttu-id="c5535-125">PSManagementGroup 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="c5535-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="c5535-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c5535-126">NOTES</span></span>

## <span data-ttu-id="c5535-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5535-127">RELATED LINKS</span></span>

[<span data-ttu-id="c5535-128">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c5535-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="c5535-129">AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c5535-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


