---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerserviceconfig
schema: 2.0.0
ms.openlocfilehash: 4a6f30d1f958094267b4ba8ddf09eb2e342ee889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802110"
---
# <span data-ttu-id="e35dd-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="e35dd-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="e35dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e35dd-102">SYNOPSIS</span></span>
<span data-ttu-id="e35dd-103">建立容器服務的本機設定物件。</span><span class="sxs-lookup"><span data-stu-id="e35dd-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e35dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="e35dd-104">SYNTAX</span></span>

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

## <span data-ttu-id="e35dd-105">說明</span><span class="sxs-lookup"><span data-stu-id="e35dd-105">DESCRIPTION</span></span>
<span data-ttu-id="e35dd-106">**新的-AzureRmContainerServiceConfig** Cmdlet 會為容器服務建立本機設定物件。</span><span class="sxs-lookup"><span data-stu-id="e35dd-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="e35dd-107">將此物件提供給 New-AzureRmContainerService Cmdlet，以建立容器服務。</span><span class="sxs-lookup"><span data-stu-id="e35dd-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="e35dd-108">示例</span><span class="sxs-lookup"><span data-stu-id="e35dd-108">EXAMPLES</span></span>

### <span data-ttu-id="e35dd-109">範例1：建立容器服務設定</span><span class="sxs-lookup"><span data-stu-id="e35dd-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="e35dd-110">這個命令會建立一個容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="e35dd-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="e35dd-111">此命令會為容器服務設定指定各種設定。</span><span class="sxs-lookup"><span data-stu-id="e35dd-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="e35dd-112">命令會使用管線運算子，將 configuration 物件傳遞到 Add-AzureRmContainerServiceAgentPoolProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e35dd-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="e35dd-113">該 Cmdlet 會新增代理池設定檔。</span><span class="sxs-lookup"><span data-stu-id="e35dd-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="e35dd-114">在 $Container 中為 **AzureRmContainerService** 的 *ContainerService* 參數指定物件。</span><span class="sxs-lookup"><span data-stu-id="e35dd-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="e35dd-115">參數</span><span class="sxs-lookup"><span data-stu-id="e35dd-115">PARAMETERS</span></span>

### <span data-ttu-id="e35dd-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="e35dd-116">-AdminUsername</span></span>
<span data-ttu-id="e35dd-117">指定要用於 Linux 基礎容器服務的系統管理員帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e35dd-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e35dd-118">-AgentPoolProfile</span></span>
<span data-ttu-id="e35dd-119">指定容器服務的代理池設定檔物件陣列。</span><span class="sxs-lookup"><span data-stu-id="e35dd-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="e35dd-120">使用 Add-AzureRmContainerServiceAgentPoolProfile Cmdlet 新增設定檔。</span><span class="sxs-lookup"><span data-stu-id="e35dd-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="e35dd-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="e35dd-122">指定自訂設定檔 orchestrator。</span><span class="sxs-lookup"><span data-stu-id="e35dd-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35dd-123">-DefaultProfile</span></span>
<span data-ttu-id="e35dd-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e35dd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-125">-位置</span><span class="sxs-lookup"><span data-stu-id="e35dd-125">-Location</span></span>
<span data-ttu-id="e35dd-126">指定要建立容器服務的位置。</span><span class="sxs-lookup"><span data-stu-id="e35dd-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="e35dd-127">-MasterCount</span></span>
<span data-ttu-id="e35dd-128">指定要建立的主虛擬機器數目。</span><span class="sxs-lookup"><span data-stu-id="e35dd-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="e35dd-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="e35dd-130">指定主虛擬機器的 DNS 前置詞。</span><span class="sxs-lookup"><span data-stu-id="e35dd-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="e35dd-131">-OrchestratorType</span></span>
<span data-ttu-id="e35dd-132">指定容器服務的 orchestrator 類型。</span><span class="sxs-lookup"><span data-stu-id="e35dd-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="e35dd-133">此參數可接受的值為： DCOS 和 Swarm。</span><span class="sxs-lookup"><span data-stu-id="e35dd-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: ContainerServiceOrchestratorTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="e35dd-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="e35dd-135">指定主體設定檔用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="e35dd-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="e35dd-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="e35dd-137">指定主體設定檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="e35dd-137">Specifies the principal profile secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e35dd-138">-SshPublicKey</span></span>
<span data-ttu-id="e35dd-139">指定以 Linux 為基礎的容器服務的 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="e35dd-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="e35dd-140">-Tag</span></span>
<span data-ttu-id="e35dd-141">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="e35dd-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e35dd-142">例如：</span><span class="sxs-lookup"><span data-stu-id="e35dd-142">For example:</span></span>

<span data-ttu-id="e35dd-143">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e35dd-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-144">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="e35dd-144">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="e35dd-145">指示此設定是否為容器服務虛擬機器啟用診斷程式。</span><span class="sxs-lookup"><span data-stu-id="e35dd-145">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-146">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="e35dd-146">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="e35dd-147">指定使用 Windows 作業系統之容器服務的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="e35dd-147">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-148">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="e35dd-148">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="e35dd-149">指定使用 Windows 作業系統之容器服務的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="e35dd-149">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-150">-確認</span><span class="sxs-lookup"><span data-stu-id="e35dd-150">-Confirm</span></span>
<span data-ttu-id="e35dd-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e35dd-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e35dd-152">-WhatIf</span></span>
<span data-ttu-id="e35dd-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e35dd-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e35dd-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e35dd-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35dd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35dd-155">CommonParameters</span></span>
<span data-ttu-id="e35dd-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e35dd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35dd-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e35dd-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35dd-158">輸入</span><span class="sxs-lookup"><span data-stu-id="e35dd-158">INPUTS</span></span>

### <span data-ttu-id="e35dd-159">所有</span><span class="sxs-lookup"><span data-stu-id="e35dd-159">None</span></span>
<span data-ttu-id="e35dd-160">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e35dd-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e35dd-161">輸出</span><span class="sxs-lookup"><span data-stu-id="e35dd-161">OUTPUTS</span></span>

### <span data-ttu-id="e35dd-162">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="e35dd-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e35dd-163">筆記</span><span class="sxs-lookup"><span data-stu-id="e35dd-163">NOTES</span></span>

## <span data-ttu-id="e35dd-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="e35dd-164">RELATED LINKS</span></span>

[<span data-ttu-id="e35dd-165">附加 AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e35dd-165">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="e35dd-166">新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e35dd-166">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)
