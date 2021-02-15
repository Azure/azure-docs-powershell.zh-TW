---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142478"
---
# <span data-ttu-id="dde6c-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="dde6c-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="dde6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dde6c-102">SYNOPSIS</span></span>
<span data-ttu-id="dde6c-103">更新 SignalR 服務的網路 ACL。</span><span class="sxs-lookup"><span data-stu-id="dde6c-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="dde6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="dde6c-104">SYNTAX</span></span>

### <span data-ttu-id="dde6c-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dde6c-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dde6c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dde6c-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dde6c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dde6c-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dde6c-108">說明</span><span class="sxs-lookup"><span data-stu-id="dde6c-108">DESCRIPTION</span></span>
<span data-ttu-id="dde6c-109">更新 SignalR 服務的網路 ACL，包括預設動作和公用及私人連線的網路 Acl。</span><span class="sxs-lookup"><span data-stu-id="dde6c-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="dde6c-110">示例</span><span class="sxs-lookup"><span data-stu-id="dde6c-110">EXAMPLES</span></span>

### <span data-ttu-id="dde6c-111">允許 RESTAPI、ClientConnection 公用網路，並將預設動作設定為 [拒絕]</span><span class="sxs-lookup"><span data-stu-id="dde6c-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -DefaultAction Deny -PublicNetwork -Allow RESTAPI,ClientConnection

PS C:\>  $networkAcl

DefaultAction PublicNetwork                                        PrivateEndpoints
------------- -------------                                        ----------------
Deny          Microsoft.Azure.Commands.SignalR.Models.PSNetworkAcl {pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1}

PS C:\> $networkAcl.PublicNetwork
Allow                       Deny
-----                       ----
{ClientConnection, RESTAPI} {}
```

### <span data-ttu-id="dde6c-112">針對私人端點連線允許用戶端連線與伺服器連線</span><span class="sxs-lookup"><span data-stu-id="dde6c-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="dde6c-113">拒絕公用網路和私人端點連線的用戶端連線</span><span class="sxs-lookup"><span data-stu-id="dde6c-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="dde6c-114">參數</span><span class="sxs-lookup"><span data-stu-id="dde6c-114">PARAMETERS</span></span>

### <span data-ttu-id="dde6c-115">-允許</span><span class="sxs-lookup"><span data-stu-id="dde6c-115">-Allow</span></span>
<span data-ttu-id="dde6c-116">允許的網路 Acl</span><span class="sxs-lookup"><span data-stu-id="dde6c-116">Allowed network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dde6c-117">-AsJob</span></span>
<span data-ttu-id="dde6c-118">在背景作業中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dde6c-118">Run the cmdlet in background job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="dde6c-119">-DefaultAction</span></span>
<span data-ttu-id="dde6c-120">SignalR 網路 Acl 的預設動作是 [允許] 或 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="dde6c-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="dde6c-121">它會決定 [拒絕網路 Acl] 或 [允許網路 Acl] 是否會生效。</span><span class="sxs-lookup"><span data-stu-id="dde6c-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="dde6c-122">例如，如果預設動作為 [允許]，則只有 [拒絕] Acl 所需的事項。</span><span class="sxs-lookup"><span data-stu-id="dde6c-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde6c-123">-DefaultProfile</span></span>
<span data-ttu-id="dde6c-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dde6c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dde6c-125">-拒絕</span><span class="sxs-lookup"><span data-stu-id="dde6c-125">-Deny</span></span>
<span data-ttu-id="dde6c-126">遭到拒絕的網路 Acl</span><span class="sxs-lookup"><span data-stu-id="dde6c-126">Denied network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dde6c-127">-InputObject</span></span>
<span data-ttu-id="dde6c-128">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="dde6c-128">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="dde6c-129">-Name</span></span>
<span data-ttu-id="dde6c-130">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="dde6c-130">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="dde6c-131">-PrivateEndpointName</span></span>
<span data-ttu-id="dde6c-132">要更新之私人端點 () s) 的名稱 (s</span><span class="sxs-lookup"><span data-stu-id="dde6c-132">Name(s) of private endpoint(s) to be updated</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="dde6c-133">-PublicNetwork</span></span>
<span data-ttu-id="dde6c-134">更新公用網路 Acl</span><span class="sxs-lookup"><span data-stu-id="dde6c-134">Update public network ACLs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde6c-135">-ResourceGroupName</span></span>
<span data-ttu-id="dde6c-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dde6c-136">The resource group name.</span></span>
<span data-ttu-id="dde6c-137">如果沒有指定，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="dde6c-137">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dde6c-138">-ResourceId</span></span>
<span data-ttu-id="dde6c-139">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dde6c-139">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-140">-確認</span><span class="sxs-lookup"><span data-stu-id="dde6c-140">-Confirm</span></span>
<span data-ttu-id="dde6c-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dde6c-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dde6c-142">-WhatIf</span></span>
<span data-ttu-id="dde6c-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dde6c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dde6c-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dde6c-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde6c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde6c-145">CommonParameters</span></span>
<span data-ttu-id="dde6c-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dde6c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde6c-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dde6c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde6c-148">輸入</span><span class="sxs-lookup"><span data-stu-id="dde6c-148">INPUTS</span></span>

### <span data-ttu-id="dde6c-149">System.object</span><span class="sxs-lookup"><span data-stu-id="dde6c-149">System.String</span></span>

## <span data-ttu-id="dde6c-150">輸出</span><span class="sxs-lookup"><span data-stu-id="dde6c-150">OUTPUTS</span></span>

### <span data-ttu-id="dde6c-151">PSSignalRNetworkAcls 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="dde6c-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="dde6c-152">筆記</span><span class="sxs-lookup"><span data-stu-id="dde6c-152">NOTES</span></span>

## <span data-ttu-id="dde6c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="dde6c-153">RELATED LINKS</span></span>
