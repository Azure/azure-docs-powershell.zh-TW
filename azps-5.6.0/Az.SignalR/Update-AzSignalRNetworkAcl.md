---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: 24552172c0f793c8414b5abfc9e6a66c747915d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902757"
---
# <span data-ttu-id="4ea05-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="4ea05-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="4ea05-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4ea05-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea05-103">更新訊號R 服務的網路 ACL。</span><span class="sxs-lookup"><span data-stu-id="4ea05-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="4ea05-104">語法</span><span class="sxs-lookup"><span data-stu-id="4ea05-104">SYNTAX</span></span>

### <span data-ttu-id="4ea05-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4ea05-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ea05-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ea05-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ea05-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ea05-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ea05-108">描述</span><span class="sxs-lookup"><span data-stu-id="4ea05-108">DESCRIPTION</span></span>
<span data-ttu-id="4ea05-109">更新 SignalR 服務的網路 ACL，包括預設動作以及公用與私人連接的網路 Acl。</span><span class="sxs-lookup"><span data-stu-id="4ea05-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="4ea05-110">例子</span><span class="sxs-lookup"><span data-stu-id="4ea05-110">EXAMPLES</span></span>

### <span data-ttu-id="4ea05-111">允許公用網路的 RESTAPI、ClientConnection，並設定預設動作為拒絕</span><span class="sxs-lookup"><span data-stu-id="4ea05-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
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

### <span data-ttu-id="4ea05-112">允許私人端點連接的用戶端連接和伺服器連接</span><span class="sxs-lookup"><span data-stu-id="4ea05-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="4ea05-113">拒絕公用網路和私人端點連接的用戶端連接</span><span class="sxs-lookup"><span data-stu-id="4ea05-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="4ea05-114">參數</span><span class="sxs-lookup"><span data-stu-id="4ea05-114">PARAMETERS</span></span>

### <span data-ttu-id="4ea05-115">-允許</span><span class="sxs-lookup"><span data-stu-id="4ea05-115">-Allow</span></span>
<span data-ttu-id="4ea05-116">允許的網路 ACL</span><span class="sxs-lookup"><span data-stu-id="4ea05-116">Allowed network ACLs</span></span>

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

### <span data-ttu-id="4ea05-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ea05-117">-AsJob</span></span>
<span data-ttu-id="4ea05-118">在背景工作中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ea05-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="4ea05-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="4ea05-119">-DefaultAction</span></span>
<span data-ttu-id="4ea05-120">SignalR 網路 ACL 的預設動作，允許或拒絕。</span><span class="sxs-lookup"><span data-stu-id="4ea05-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="4ea05-121">它會決定是否要拒絕網路 ACL 或允許網路 ACL 生效。</span><span class="sxs-lookup"><span data-stu-id="4ea05-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="4ea05-122">例如，如果預設動作為允許，則只有拒絕 ACL 很重要。</span><span class="sxs-lookup"><span data-stu-id="4ea05-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

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

### <span data-ttu-id="4ea05-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea05-123">-DefaultProfile</span></span>
<span data-ttu-id="4ea05-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ea05-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ea05-125">-拒絕</span><span class="sxs-lookup"><span data-stu-id="4ea05-125">-Deny</span></span>
<span data-ttu-id="4ea05-126">拒絕的網路 ACL</span><span class="sxs-lookup"><span data-stu-id="4ea05-126">Denied network ACLs</span></span>

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

### <span data-ttu-id="4ea05-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ea05-127">-InputObject</span></span>
<span data-ttu-id="4ea05-128">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="4ea05-128">The SignalR resource object.</span></span>

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

### <span data-ttu-id="4ea05-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ea05-129">-Name</span></span>
<span data-ttu-id="4ea05-130">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="4ea05-130">The SignalR service name.</span></span>

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

### <span data-ttu-id="4ea05-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="4ea05-131">-PrivateEndpointName</span></span>
<span data-ttu-id="4ea05-132">為 (更新) 之 (端點) 名稱</span><span class="sxs-lookup"><span data-stu-id="4ea05-132">Name(s) of private endpoint(s) to be updated</span></span>

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

### <span data-ttu-id="4ea05-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="4ea05-133">-PublicNetwork</span></span>
<span data-ttu-id="4ea05-134">更新公用網路 ACL</span><span class="sxs-lookup"><span data-stu-id="4ea05-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="4ea05-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea05-135">-ResourceGroupName</span></span>
<span data-ttu-id="4ea05-136">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4ea05-136">The resource group name.</span></span>
<span data-ttu-id="4ea05-137">如果沒有指定，將會使用預設選項。</span><span class="sxs-lookup"><span data-stu-id="4ea05-137">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="4ea05-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ea05-138">-ResourceId</span></span>
<span data-ttu-id="4ea05-139">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ea05-139">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="4ea05-140">-確認</span><span class="sxs-lookup"><span data-stu-id="4ea05-140">-Confirm</span></span>
<span data-ttu-id="4ea05-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4ea05-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea05-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea05-142">-WhatIf</span></span>
<span data-ttu-id="4ea05-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ea05-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea05-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ea05-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea05-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea05-145">CommonParameters</span></span>
<span data-ttu-id="4ea05-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4ea05-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea05-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ea05-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea05-148">輸入</span><span class="sxs-lookup"><span data-stu-id="4ea05-148">INPUTS</span></span>

### <span data-ttu-id="4ea05-149">System.String</span><span class="sxs-lookup"><span data-stu-id="4ea05-149">System.String</span></span>

## <span data-ttu-id="4ea05-150">輸出</span><span class="sxs-lookup"><span data-stu-id="4ea05-150">OUTPUTS</span></span>

### <span data-ttu-id="4ea05-151">Microsoft.Azure.Commands.SignalR.models.PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="4ea05-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="4ea05-152">筆記</span><span class="sxs-lookup"><span data-stu-id="4ea05-152">NOTES</span></span>

## <span data-ttu-id="4ea05-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ea05-153">RELATED LINKS</span></span>
