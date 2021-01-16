---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284372"
---
# <span data-ttu-id="d8a93-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="d8a93-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="d8a93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8a93-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a93-103">取得或列出工作區的連結服務</span><span class="sxs-lookup"><span data-stu-id="d8a93-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="d8a93-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8a93-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8a93-105">說明</span><span class="sxs-lookup"><span data-stu-id="d8a93-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a93-106">[取得或列出工作區的連結服務]、[未提供 "-LinkedServiceName] 的清單</span><span class="sxs-lookup"><span data-stu-id="d8a93-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="d8a93-107">示例</span><span class="sxs-lookup"><span data-stu-id="d8a93-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a93-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d8a93-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="d8a93-109">取得工作區的連結服務</span><span class="sxs-lookup"><span data-stu-id="d8a93-109">Get linked service for workspace</span></span>

## <span data-ttu-id="d8a93-110">參數</span><span class="sxs-lookup"><span data-stu-id="d8a93-110">PARAMETERS</span></span>

### <span data-ttu-id="d8a93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a93-111">-DefaultProfile</span></span>
<span data-ttu-id="d8a93-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8a93-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a93-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="d8a93-113">-LinkedServiceName</span></span>
<span data-ttu-id="d8a93-114">連結的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="d8a93-114">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a93-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8a93-115">-ResourceGroupName</span></span>
<span data-ttu-id="d8a93-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8a93-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a93-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8a93-117">-WorkspaceName</span></span>
<span data-ttu-id="d8a93-118">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="d8a93-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a93-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a93-119">CommonParameters</span></span>
<span data-ttu-id="d8a93-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8a93-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a93-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d8a93-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a93-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d8a93-122">INPUTS</span></span>

### <span data-ttu-id="d8a93-123">System.object</span><span class="sxs-lookup"><span data-stu-id="d8a93-123">System.String</span></span>

## <span data-ttu-id="d8a93-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d8a93-124">OUTPUTS</span></span>

### <span data-ttu-id="d8a93-125">PSLinkedService 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="d8a93-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="d8a93-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d8a93-126">NOTES</span></span>

## <span data-ttu-id="d8a93-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8a93-127">RELATED LINKS</span></span>
