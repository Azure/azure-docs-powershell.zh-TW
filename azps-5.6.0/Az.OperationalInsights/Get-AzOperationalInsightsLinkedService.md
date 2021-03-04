---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 71a715386a4d5646f1c9015244ad8a096313bb64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905322"
---
# <span data-ttu-id="2f745-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="2f745-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="2f745-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f745-102">SYNOPSIS</span></span>
<span data-ttu-id="2f745-103">取得或列出工作區的連結服務</span><span class="sxs-lookup"><span data-stu-id="2f745-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="2f745-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f745-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f745-105">描述</span><span class="sxs-lookup"><span data-stu-id="2f745-105">DESCRIPTION</span></span>
<span data-ttu-id="2f745-106">取得或列出工作區的連結服務，未提供 「-LinkedServiceName」時的清單</span><span class="sxs-lookup"><span data-stu-id="2f745-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="2f745-107">例子</span><span class="sxs-lookup"><span data-stu-id="2f745-107">EXAMPLES</span></span>

### <span data-ttu-id="2f745-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2f745-108">Example 1</span></span>
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

<span data-ttu-id="2f745-109">取得工作區的連結服務</span><span class="sxs-lookup"><span data-stu-id="2f745-109">Get linked service for workspace</span></span>

## <span data-ttu-id="2f745-110">參數</span><span class="sxs-lookup"><span data-stu-id="2f745-110">PARAMETERS</span></span>

### <span data-ttu-id="2f745-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f745-111">-DefaultProfile</span></span>
<span data-ttu-id="2f745-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f745-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f745-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="2f745-113">-LinkedServiceName</span></span>
<span data-ttu-id="2f745-114">連結的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="2f745-114">The linked service name.</span></span>

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

### <span data-ttu-id="2f745-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f745-115">-ResourceGroupName</span></span>
<span data-ttu-id="2f745-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2f745-116">The resource group name.</span></span>

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

### <span data-ttu-id="2f745-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2f745-117">-WorkspaceName</span></span>
<span data-ttu-id="2f745-118">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="2f745-118">The workspace name.</span></span>

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

### <span data-ttu-id="2f745-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f745-119">CommonParameters</span></span>
<span data-ttu-id="2f745-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f745-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f745-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f745-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f745-122">輸入</span><span class="sxs-lookup"><span data-stu-id="2f745-122">INPUTS</span></span>

### <span data-ttu-id="2f745-123">System.String</span><span class="sxs-lookup"><span data-stu-id="2f745-123">System.String</span></span>

## <span data-ttu-id="2f745-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2f745-124">OUTPUTS</span></span>

### <span data-ttu-id="2f745-125">Microsoft.Azure.Commands.OperationalInsights.models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="2f745-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="2f745-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2f745-126">NOTES</span></span>

## <span data-ttu-id="2f745-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f745-127">RELATED LINKS</span></span>
