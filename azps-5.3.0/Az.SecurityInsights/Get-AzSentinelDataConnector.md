---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448571"
---
# <span data-ttu-id="a1b20-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="a1b20-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="a1b20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1b20-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b20-103">取得資料連線器。</span><span class="sxs-lookup"><span data-stu-id="a1b20-103">Get a Data Connector.</span></span>

## <span data-ttu-id="a1b20-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1b20-104">SYNTAX</span></span>

### <span data-ttu-id="a1b20-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="a1b20-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1b20-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="a1b20-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1b20-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b20-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1b20-108">說明</span><span class="sxs-lookup"><span data-stu-id="a1b20-108">DESCRIPTION</span></span>
<span data-ttu-id="a1b20-109">**AzSentinelDataConnector** Cmdlet 會從指定的工作區取得資料連線器。</span><span class="sxs-lookup"><span data-stu-id="a1b20-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="a1b20-110">如果您指定 *DataConnectorId* 參數，則會傳回單一 **DataConnector** 物件。</span><span class="sxs-lookup"><span data-stu-id="a1b20-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="a1b20-111">如果您沒有指定 *DataConnectorId* 參數，則會傳回包含指定工作區中所有資料連線器的陣列。</span><span class="sxs-lookup"><span data-stu-id="a1b20-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="a1b20-112">您可以使用 **DataConnector** 物件來更新資料連線器，例如，您可以停用 **DataConnector**。</span><span class="sxs-lookup"><span data-stu-id="a1b20-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="a1b20-113">示例</span><span class="sxs-lookup"><span data-stu-id="a1b20-113">EXAMPLES</span></span>

### <span data-ttu-id="a1b20-114">範例1</span><span class="sxs-lookup"><span data-stu-id="a1b20-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="a1b20-115">這個範例會在指定的工作區中取得所有 **DataConnectors** ，然後將它儲存在 $DataConnectors 變數中。</span><span class="sxs-lookup"><span data-stu-id="a1b20-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="a1b20-116">範例2</span><span class="sxs-lookup"><span data-stu-id="a1b20-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="a1b20-117">這個範例會在指定的工作區中取得 **DataConnector** ，然後將其儲存在 $DataConnector 變數中。</span><span class="sxs-lookup"><span data-stu-id="a1b20-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="a1b20-118">參數</span><span class="sxs-lookup"><span data-stu-id="a1b20-118">PARAMETERS</span></span>

### <span data-ttu-id="a1b20-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="a1b20-119">-DataConnectorId</span></span>
<span data-ttu-id="a1b20-120">資料連線器識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1b20-120">Data Connector Id.</span></span>

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

### <span data-ttu-id="a1b20-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b20-121">-DefaultProfile</span></span>
<span data-ttu-id="a1b20-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1b20-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b20-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b20-123">-ResourceGroupName</span></span>
<span data-ttu-id="a1b20-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a1b20-124">Resource group name.</span></span>

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

### <span data-ttu-id="a1b20-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b20-125">-ResourceId</span></span>
<span data-ttu-id="a1b20-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a1b20-126">Resource Id.</span></span>

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

### <span data-ttu-id="a1b20-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a1b20-127">-WorkspaceName</span></span>
<span data-ttu-id="a1b20-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="a1b20-128">Workspace Name.</span></span>

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

### <span data-ttu-id="a1b20-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b20-129">CommonParameters</span></span>
<span data-ttu-id="a1b20-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1b20-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b20-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a1b20-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b20-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a1b20-132">INPUTS</span></span>

### <span data-ttu-id="a1b20-133">System.object</span><span class="sxs-lookup"><span data-stu-id="a1b20-133">System.String</span></span>
## <span data-ttu-id="a1b20-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a1b20-134">OUTPUTS</span></span>

### <span data-ttu-id="a1b20-135">SecurityInsights DataConnectors. PSSentinelDataConnector （）</span><span class="sxs-lookup"><span data-stu-id="a1b20-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="a1b20-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a1b20-136">NOTES</span></span>

## <span data-ttu-id="a1b20-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1b20-137">RELATED LINKS</span></span>
