---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: a2d55c831860f5664f0f8f3dd5312368a9e5da4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138236"
---
# <span data-ttu-id="8d865-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="8d865-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="8d865-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d865-102">SYNOPSIS</span></span>
<span data-ttu-id="8d865-103">建立容器服務的本機設定物件。</span><span class="sxs-lookup"><span data-stu-id="8d865-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="8d865-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d865-104">SYNTAX</span></span>

```
New-AzContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d865-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d865-105">DESCRIPTION</span></span>
<span data-ttu-id="8d865-106">**新的-AzContainerServiceConfig** Cmdlet 會為容器服務建立本機設定物件。</span><span class="sxs-lookup"><span data-stu-id="8d865-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="8d865-107">將此物件提供給 New-AzContainerService Cmdlet，以建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="8d865-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="8d865-108">示例</span><span class="sxs-lookup"><span data-stu-id="8d865-108">EXAMPLES</span></span>

### <span data-ttu-id="8d865-109">範例1：建立容器服務設定</span><span class="sxs-lookup"><span data-stu-id="8d865-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="8d865-110">這個命令會建立一個容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="8d865-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8d865-111">此命令會為容器服務設定指定各種設定。</span><span class="sxs-lookup"><span data-stu-id="8d865-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="8d865-112">命令會使用管線運算子，將 configuration 物件傳遞到 Add-AzContainerServiceAgentPoolProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d865-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="8d865-113">該 Cmdlet 會新增代理池設定檔。</span><span class="sxs-lookup"><span data-stu-id="8d865-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="8d865-114">在 $Container 中為 **AzContainerService** 的 *ContainerService* 參數指定物件。</span><span class="sxs-lookup"><span data-stu-id="8d865-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="8d865-115">參數</span><span class="sxs-lookup"><span data-stu-id="8d865-115">PARAMETERS</span></span>

### <span data-ttu-id="8d865-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="8d865-116">-AdminUsername</span></span>
<span data-ttu-id="8d865-117">指定要用於 Linux 基礎容器服務的系統管理員帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8d865-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="8d865-118">-AgentPoolProfile</span></span>
<span data-ttu-id="8d865-119">指定容器服務的代理池設定檔物件陣列。</span><span class="sxs-lookup"><span data-stu-id="8d865-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="8d865-120">使用 Add-AzContainerServiceAgentPoolProfile Cmdlet 新增設定檔。</span><span class="sxs-lookup"><span data-stu-id="8d865-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="8d865-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="8d865-122">指定自訂設定檔 orchestrator。</span><span class="sxs-lookup"><span data-stu-id="8d865-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d865-123">-DefaultProfile</span></span>
<span data-ttu-id="8d865-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d865-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d865-125">-位置</span><span class="sxs-lookup"><span data-stu-id="8d865-125">-Location</span></span>
<span data-ttu-id="8d865-126">指定要建立容器服務的位置。</span><span class="sxs-lookup"><span data-stu-id="8d865-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="8d865-127">-MasterCount</span></span>
<span data-ttu-id="8d865-128">指定要建立的主虛擬機器數目。</span><span class="sxs-lookup"><span data-stu-id="8d865-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="8d865-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="8d865-130">指定主虛擬機器的 DNS 前置詞。</span><span class="sxs-lookup"><span data-stu-id="8d865-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="8d865-131">-OrchestratorType</span></span>
<span data-ttu-id="8d865-132">指定容器服務的 orchestrator 類型。</span><span class="sxs-lookup"><span data-stu-id="8d865-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="8d865-133">此參數可接受的值為： DCOS 和 Swarm。</span><span class="sxs-lookup"><span data-stu-id="8d865-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="8d865-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="8d865-135">指定主體設定檔用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d865-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="8d865-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="8d865-137">指定主體設定檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="8d865-137">Specifies the principal profile secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="8d865-138">-SshPublicKey</span></span>
<span data-ttu-id="8d865-139">指定以 Linux 為基礎的容器服務的 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="8d865-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="8d865-140">-Tag</span></span>
<span data-ttu-id="8d865-141">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="8d865-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8d865-142">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8d865-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="8d865-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="8d865-144">指示此設定是否為容器服務虛擬機器啟用診斷程式。</span><span class="sxs-lookup"><span data-stu-id="8d865-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="8d865-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="8d865-146">指定使用 Windows 作業系統之容器服務的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="8d865-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="8d865-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="8d865-148">指定使用 Windows 作業系統之容器服務的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="8d865-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d865-149">-確認</span><span class="sxs-lookup"><span data-stu-id="8d865-149">-Confirm</span></span>
<span data-ttu-id="8d865-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d865-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d865-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d865-151">-WhatIf</span></span>
<span data-ttu-id="8d865-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d865-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d865-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d865-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d865-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d865-154">CommonParameters</span></span>
<span data-ttu-id="8d865-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d865-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d865-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d865-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d865-157">輸入</span><span class="sxs-lookup"><span data-stu-id="8d865-157">INPUTS</span></span>

### <span data-ttu-id="8d865-158">System.object</span><span class="sxs-lookup"><span data-stu-id="8d865-158">System.String</span></span>

### <span data-ttu-id="8d865-159">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8d865-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8d865-160">"ContainerServiceOrchestratorTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="8d865-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8d865-161">System.object</span><span class="sxs-lookup"><span data-stu-id="8d865-161">System.Int32</span></span>

### <span data-ttu-id="8d865-162">ContainerServiceAgentPoolProfile [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="8d865-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="8d865-163">System.object []</span><span class="sxs-lookup"><span data-stu-id="8d865-163">System.String[]</span></span>

### <span data-ttu-id="8d865-164">System.object</span><span class="sxs-lookup"><span data-stu-id="8d865-164">System.Boolean</span></span>

## <span data-ttu-id="8d865-165">輸出</span><span class="sxs-lookup"><span data-stu-id="8d865-165">OUTPUTS</span></span>

### <span data-ttu-id="8d865-166">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="8d865-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="8d865-167">筆記</span><span class="sxs-lookup"><span data-stu-id="8d865-167">NOTES</span></span>

## <span data-ttu-id="8d865-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d865-168">RELATED LINKS</span></span>

[<span data-ttu-id="8d865-169">附加 AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="8d865-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="8d865-170">新-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="8d865-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
