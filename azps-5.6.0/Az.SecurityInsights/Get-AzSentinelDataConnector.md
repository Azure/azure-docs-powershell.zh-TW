---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: b99ad26ddfa0239f073c4179413b2f1fefec4d1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910609"
---
# <span data-ttu-id="f8120-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="f8120-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="f8120-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f8120-102">SYNOPSIS</span></span>
<span data-ttu-id="f8120-103">取得資料連線器。</span><span class="sxs-lookup"><span data-stu-id="f8120-103">Get a Data Connector.</span></span>

## <span data-ttu-id="f8120-104">語法</span><span class="sxs-lookup"><span data-stu-id="f8120-104">SYNTAX</span></span>

### <span data-ttu-id="f8120-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="f8120-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8120-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="f8120-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8120-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8120-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8120-108">描述</span><span class="sxs-lookup"><span data-stu-id="f8120-108">DESCRIPTION</span></span>
<span data-ttu-id="f8120-109">**Get-AzSentinelDataConnector** Cmdlet 會從指定的工作區取得資料連線器。</span><span class="sxs-lookup"><span data-stu-id="f8120-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="f8120-110">如果您指定 *DataConnectorId* 參數，會返回單 **一 DataConnector** 物件。</span><span class="sxs-lookup"><span data-stu-id="f8120-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="f8120-111">如果您未指定 *DataConnectorId* 參數，則會返回包含指定工作區中所有資料連線器的陣列。</span><span class="sxs-lookup"><span data-stu-id="f8120-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="f8120-112">您可以使用 **DataConnector 物件** 來更新資料連線器，例如，您可以停用 **DataConnector。**</span><span class="sxs-lookup"><span data-stu-id="f8120-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="f8120-113">例子</span><span class="sxs-lookup"><span data-stu-id="f8120-113">EXAMPLES</span></span>

### <span data-ttu-id="f8120-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="f8120-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="f8120-115">此範例會獲得指定 **工作區中所有的 DataConnectors，** 然後將它儲存在$DataConnectors變數。</span><span class="sxs-lookup"><span data-stu-id="f8120-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="f8120-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="f8120-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="f8120-117">此範例會獲得 **指定工作區中的 DataConnector，** 然後將它儲存在$DataConnector變數中。</span><span class="sxs-lookup"><span data-stu-id="f8120-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="f8120-118">參數</span><span class="sxs-lookup"><span data-stu-id="f8120-118">PARAMETERS</span></span>

### <span data-ttu-id="f8120-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="f8120-119">-DataConnectorId</span></span>
<span data-ttu-id="f8120-120">資料連線器識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8120-120">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8120-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8120-121">-DefaultProfile</span></span>
<span data-ttu-id="f8120-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8120-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8120-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8120-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8120-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f8120-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8120-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8120-125">-ResourceId</span></span>
<span data-ttu-id="f8120-126">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8120-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8120-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f8120-127">-WorkspaceName</span></span>
<span data-ttu-id="f8120-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="f8120-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8120-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8120-129">CommonParameters</span></span>
<span data-ttu-id="f8120-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f8120-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8120-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8120-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8120-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f8120-132">INPUTS</span></span>

### <span data-ttu-id="f8120-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f8120-133">System.String</span></span>
## <span data-ttu-id="f8120-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f8120-134">OUTPUTS</span></span>

### <span data-ttu-id="f8120-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="f8120-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="f8120-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f8120-136">NOTES</span></span>

## <span data-ttu-id="f8120-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8120-137">RELATED LINKS</span></span>
