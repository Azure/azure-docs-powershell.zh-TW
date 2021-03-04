---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 505156f1c6303b8a3fa699b5528ed3ca2ff690de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911877"
---
# <span data-ttu-id="4cf5d-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4cf5d-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="4cf5d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4cf5d-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf5d-103">獲得連接至工作區的管理群組詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4cf5d-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="4cf5d-104">語法</span><span class="sxs-lookup"><span data-stu-id="4cf5d-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cf5d-105">描述</span><span class="sxs-lookup"><span data-stu-id="4cf5d-105">DESCRIPTION</span></span>
<span data-ttu-id="4cf5d-106">**Get-AzOperationalInsightsWorkspaceManagementGroup** Cmdlet 會列出連接至工作區的管理群組。</span><span class="sxs-lookup"><span data-stu-id="4cf5d-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="4cf5d-107">例子</span><span class="sxs-lookup"><span data-stu-id="4cf5d-107">EXAMPLES</span></span>

### <span data-ttu-id="4cf5d-108">範例 1：根據工作區名稱取得管理群組</span><span class="sxs-lookup"><span data-stu-id="4cf5d-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="4cf5d-109">此命令會針對名為 ContosoResourceGroup 的資源群組中名為 MyWorkspace 的工作區，獲得管理群組。</span><span class="sxs-lookup"><span data-stu-id="4cf5d-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="4cf5d-110">範例 2：使用管線取得管理群組</span><span class="sxs-lookup"><span data-stu-id="4cf5d-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="4cf5d-111">此命令使用 Get-AzOperationalInsightsWorkspace Cmdlet 取得名為 MyWorkspace 的工作區，然後將工作區傳遞至目前的 Cmdlet，這會取得該工作區的管理群組。</span><span class="sxs-lookup"><span data-stu-id="4cf5d-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="4cf5d-112">參數</span><span class="sxs-lookup"><span data-stu-id="4cf5d-112">PARAMETERS</span></span>

### <span data-ttu-id="4cf5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf5d-113">-DefaultProfile</span></span>
<span data-ttu-id="4cf5d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4cf5d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cf5d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cf5d-115">-Name</span></span>
<span data-ttu-id="4cf5d-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="4cf5d-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="4cf5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4cf5d-118">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cf5d-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="4cf5d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf5d-119">CommonParameters</span></span>
<span data-ttu-id="4cf5d-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4cf5d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf5d-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4cf5d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf5d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4cf5d-122">INPUTS</span></span>

### <span data-ttu-id="4cf5d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4cf5d-123">System.String</span></span>

## <span data-ttu-id="4cf5d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4cf5d-124">OUTPUTS</span></span>

### <span data-ttu-id="4cf5d-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4cf5d-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="4cf5d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4cf5d-126">NOTES</span></span>

## <span data-ttu-id="4cf5d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cf5d-127">RELATED LINKS</span></span>

[<span data-ttu-id="4cf5d-128">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4cf5d-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="4cf5d-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4cf5d-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


