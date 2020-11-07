---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: e88f1d3ce684881d839574fe0b73f36b83e275f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626508"
---
# <span data-ttu-id="36920-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="36920-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="36920-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36920-102">SYNOPSIS</span></span>
<span data-ttu-id="36920-103">建立容器服務的本機設定物件。</span><span class="sxs-lookup"><span data-stu-id="36920-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36920-104">句法</span><span class="sxs-lookup"><span data-stu-id="36920-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36920-105">說明</span><span class="sxs-lookup"><span data-stu-id="36920-105">DESCRIPTION</span></span>
<span data-ttu-id="36920-106">**新的-AzureRmContainerServiceConfig** Cmdlet 會為容器服務建立本機設定物件。</span><span class="sxs-lookup"><span data-stu-id="36920-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="36920-107">將此物件提供給 New-AzureRmContainerService Cmdlet，以建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="36920-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="36920-108">示例</span><span class="sxs-lookup"><span data-stu-id="36920-108">EXAMPLES</span></span>

### <span data-ttu-id="36920-109">範例1：建立容器服務設定</span><span class="sxs-lookup"><span data-stu-id="36920-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="36920-110">這個命令會建立一個容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="36920-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="36920-111">此命令會為容器服務設定指定各種設定。</span><span class="sxs-lookup"><span data-stu-id="36920-111">The command specifies various settings for the container service configuration.</span></span>
<span data-ttu-id="36920-112">命令會使用管線運算子，將 configuration 物件傳遞到 Add-AzureRmContainerServiceAgentPoolProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36920-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="36920-113">該 Cmdlet 會新增代理池設定檔。</span><span class="sxs-lookup"><span data-stu-id="36920-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="36920-114">在 $Container 中為 **AzureRmContainerService** 的 *ContainerService* 參數指定物件。</span><span class="sxs-lookup"><span data-stu-id="36920-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="36920-115">參數</span><span class="sxs-lookup"><span data-stu-id="36920-115">PARAMETERS</span></span>

### <span data-ttu-id="36920-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="36920-116">-AdminUsername</span></span>
<span data-ttu-id="36920-117">指定要用於 Linux 基礎容器服務的系統管理員帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="36920-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="36920-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="36920-118">-AgentPoolProfile</span></span>
<span data-ttu-id="36920-119">指定容器服務的代理池設定檔物件陣列。</span><span class="sxs-lookup"><span data-stu-id="36920-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="36920-120">使用 Add-AzureRmContainerServiceAgentPoolProfile Cmdlet 新增設定檔。</span><span class="sxs-lookup"><span data-stu-id="36920-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="36920-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="36920-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="36920-122">指定自訂設定檔 orchestrator。</span><span class="sxs-lookup"><span data-stu-id="36920-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="36920-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36920-123">-DefaultProfile</span></span>
<span data-ttu-id="36920-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="36920-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36920-125">-位置</span><span class="sxs-lookup"><span data-stu-id="36920-125">-Location</span></span>
<span data-ttu-id="36920-126">指定要建立容器服務的位置。</span><span class="sxs-lookup"><span data-stu-id="36920-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="36920-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="36920-127">-MasterCount</span></span>
<span data-ttu-id="36920-128">指定要建立的主虛擬機器數目。</span><span class="sxs-lookup"><span data-stu-id="36920-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36920-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="36920-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="36920-130">指定主虛擬機器的 DNS 前置詞。</span><span class="sxs-lookup"><span data-stu-id="36920-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="36920-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="36920-131">-OrchestratorType</span></span>
<span data-ttu-id="36920-132">指定容器服務的 orchestrator 類型。</span><span class="sxs-lookup"><span data-stu-id="36920-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="36920-133">此參數可接受的值為： DCOS 和 Swarm。</span><span class="sxs-lookup"><span data-stu-id="36920-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="36920-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="36920-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="36920-135">指定主體設定檔用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="36920-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="36920-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="36920-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="36920-137">指定主體設定檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="36920-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="36920-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="36920-138">-SshPublicKey</span></span>
<span data-ttu-id="36920-139">指定以 Linux 為基礎的容器服務的 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="36920-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="36920-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="36920-140">-Tag</span></span>
<span data-ttu-id="36920-141">指定容器服務的標記。</span><span class="sxs-lookup"><span data-stu-id="36920-141">Specifies tags for the container service.</span></span>

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

### <span data-ttu-id="36920-142">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="36920-142">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="36920-143">指示此設定是否為容器服務虛擬機器啟用診斷程式。</span><span class="sxs-lookup"><span data-stu-id="36920-143">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="36920-144">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="36920-144">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="36920-145">指定使用 Windows 作業系統之容器服務的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="36920-145">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="36920-146">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="36920-146">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="36920-147">指定使用 Windows 作業系統之容器服務的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="36920-147">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="36920-148">-確認</span><span class="sxs-lookup"><span data-stu-id="36920-148">-Confirm</span></span>
<span data-ttu-id="36920-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="36920-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36920-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36920-150">-WhatIf</span></span>
<span data-ttu-id="36920-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36920-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36920-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36920-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36920-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36920-153">CommonParameters</span></span>
<span data-ttu-id="36920-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36920-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36920-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="36920-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36920-156">輸入</span><span class="sxs-lookup"><span data-stu-id="36920-156">INPUTS</span></span>

## <span data-ttu-id="36920-157">輸出</span><span class="sxs-lookup"><span data-stu-id="36920-157">OUTPUTS</span></span>

## <span data-ttu-id="36920-158">筆記</span><span class="sxs-lookup"><span data-stu-id="36920-158">NOTES</span></span>

## <span data-ttu-id="36920-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="36920-159">RELATED LINKS</span></span>

[<span data-ttu-id="36920-160">附加 AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="36920-160">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="36920-161">新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="36920-161">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)


