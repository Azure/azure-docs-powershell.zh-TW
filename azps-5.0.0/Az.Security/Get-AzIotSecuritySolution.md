---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140914"
---
# <span data-ttu-id="abc9a-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="abc9a-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="abc9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="abc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="abc9a-103">取得 IoT 安全解決方案</span><span class="sxs-lookup"><span data-stu-id="abc9a-103">Get IoT security solution</span></span>

## <span data-ttu-id="abc9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="abc9a-104">SYNTAX</span></span>

### <span data-ttu-id="abc9a-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="abc9a-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abc9a-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="abc9a-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abc9a-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="abc9a-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abc9a-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="abc9a-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abc9a-109">說明</span><span class="sxs-lookup"><span data-stu-id="abc9a-109">DESCRIPTION</span></span>
<span data-ttu-id="abc9a-110">Get-AzIotSecuritySolution Cmdlet 會傳回一或多個 iot 安全解決方案。</span><span class="sxs-lookup"><span data-stu-id="abc9a-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="abc9a-111">IoT 安全解決方案會從 IoT 裝置和 IoT 中樞收集安全性資料和事件，以協助防範及偵測威脅。</span><span class="sxs-lookup"><span data-stu-id="abc9a-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="abc9a-112">示例</span><span class="sxs-lookup"><span data-stu-id="abc9a-112">EXAMPLES</span></span>

### <span data-ttu-id="abc9a-113">範例1</span><span class="sxs-lookup"><span data-stu-id="abc9a-113">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "centraluseuap"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="abc9a-114">在資源群組 "MyResourceGroup" 中取得「MySample」方案</span><span class="sxs-lookup"><span data-stu-id="abc9a-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="abc9a-115">範例2</span><span class="sxs-lookup"><span data-stu-id="abc9a-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="abc9a-116">取得資源群組 "MyResourceGroup" 中的所有安全性解決方案清單</span><span class="sxs-lookup"><span data-stu-id="abc9a-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="abc9a-117">參數</span><span class="sxs-lookup"><span data-stu-id="abc9a-117">PARAMETERS</span></span>

### <span data-ttu-id="abc9a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc9a-118">-DefaultProfile</span></span>
<span data-ttu-id="abc9a-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="abc9a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abc9a-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="abc9a-120">-Name</span></span>
<span data-ttu-id="abc9a-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="abc9a-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc9a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc9a-122">-ResourceGroupName</span></span>
<span data-ttu-id="abc9a-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="abc9a-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc9a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abc9a-124">-ResourceId</span></span>
<span data-ttu-id="abc9a-125">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="abc9a-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="abc9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc9a-126">CommonParameters</span></span>
<span data-ttu-id="abc9a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="abc9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc9a-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="abc9a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc9a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="abc9a-129">INPUTS</span></span>

### <span data-ttu-id="abc9a-130">System.object</span><span class="sxs-lookup"><span data-stu-id="abc9a-130">System.String</span></span>

## <span data-ttu-id="abc9a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="abc9a-131">OUTPUTS</span></span>

### <span data-ttu-id="abc9a-132">PSIotSecuritySolution 中的 IotSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="abc9a-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="abc9a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="abc9a-133">NOTES</span></span>

## <span data-ttu-id="abc9a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="abc9a-134">RELATED LINKS</span></span>