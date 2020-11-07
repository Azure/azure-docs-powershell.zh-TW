---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 55fe1a82d0e54606c04954167aef2c2b90086655
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625111"
---
# <span data-ttu-id="4208c-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="4208c-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="4208c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4208c-102">SYNOPSIS</span></span>
<span data-ttu-id="4208c-103">取得連接至工作區之管理群組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4208c-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4208c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4208c-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4208c-105">說明</span><span class="sxs-lookup"><span data-stu-id="4208c-105">DESCRIPTION</span></span>
<span data-ttu-id="4208c-106">**AzureRmOperationalInsightsWorkspaceManagementGroups** Cmdlet 會列出已連接至工作區的管理群組。</span><span class="sxs-lookup"><span data-stu-id="4208c-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="4208c-107">示例</span><span class="sxs-lookup"><span data-stu-id="4208c-107">EXAMPLES</span></span>

### <span data-ttu-id="4208c-108">範例1：依工作區名稱取得管理群組</span><span class="sxs-lookup"><span data-stu-id="4208c-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="4208c-109">這個命令會取得名為 ContosoResourceGroup 之資源群組中名為 MyWorkspace 之工作區的管理群組。</span><span class="sxs-lookup"><span data-stu-id="4208c-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="4208c-110">範例2：使用管線取得管理群組</span><span class="sxs-lookup"><span data-stu-id="4208c-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="4208c-111">這個命令會使用 Get-AzureRmOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後將工作區傳送至目前的 Cmdlet，以取得該工作區的管理群組。</span><span class="sxs-lookup"><span data-stu-id="4208c-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="4208c-112">參數</span><span class="sxs-lookup"><span data-stu-id="4208c-112">PARAMETERS</span></span>

### <span data-ttu-id="4208c-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="4208c-113">-Name</span></span>
<span data-ttu-id="4208c-114">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="4208c-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="4208c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4208c-115">-ResourceGroupName</span></span>
<span data-ttu-id="4208c-116">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4208c-116">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="4208c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4208c-117">-DefaultProfile</span></span>
<span data-ttu-id="4208c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4208c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4208c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4208c-119">CommonParameters</span></span>
<span data-ttu-id="4208c-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4208c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4208c-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4208c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4208c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4208c-122">INPUTS</span></span>

## <span data-ttu-id="4208c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="4208c-123">OUTPUTS</span></span>

### <span data-ttu-id="4208c-124">[System.object]. 清單 ' 1 [OperationalInsights]。 PSManagementGroup]</span><span class="sxs-lookup"><span data-stu-id="4208c-124">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup]</span></span>

## <span data-ttu-id="4208c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="4208c-125">NOTES</span></span>

## <span data-ttu-id="4208c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="4208c-126">RELATED LINKS</span></span>

[<span data-ttu-id="4208c-127">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4208c-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="4208c-128">AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4208c-128">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


