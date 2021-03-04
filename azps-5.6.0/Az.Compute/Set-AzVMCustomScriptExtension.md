---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 97f2c22d4e724d53c165e2e1e73ba27fce9290b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903310"
---
# <span data-ttu-id="cf415-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cf415-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="cf415-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cf415-102">SYNOPSIS</span></span>
<span data-ttu-id="cf415-103">新增自訂腳本擴充功能至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cf415-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="cf415-104">語法</span><span class="sxs-lookup"><span data-stu-id="cf415-104">SYNTAX</span></span>

### <span data-ttu-id="cf415-105">ByNameWithContainerAndFileNamesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cf415-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf415-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf415-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf415-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf415-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf415-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf415-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf415-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf415-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf415-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf415-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf415-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf415-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf415-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf415-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf415-113">描述</span><span class="sxs-lookup"><span data-stu-id="cf415-113">DESCRIPTION</span></span>
<span data-ttu-id="cf415-114">**Set-AzTOMCustomScriptExtension** Cmdlet 會新增自訂腳本虛擬機器擴充功能至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cf415-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="cf415-115">此擴充功能可讓您在虛擬機器上執行自己的腳本。</span><span class="sxs-lookup"><span data-stu-id="cf415-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="cf415-116">例子</span><span class="sxs-lookup"><span data-stu-id="cf415-116">EXAMPLES</span></span>

### <span data-ttu-id="cf415-117">範例 1：新增自訂腳本</span><span class="sxs-lookup"><span data-stu-id="cf415-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="cf415-118">此命令會將自訂腳本新增到名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cf415-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="cf415-119">腳本檔案會contososcript.exe。</span><span class="sxs-lookup"><span data-stu-id="cf415-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="cf415-120">範例 2</span><span class="sxs-lookup"><span data-stu-id="cf415-120">Example 2</span></span>

<span data-ttu-id="cf415-121">新增自訂腳本擴充功能至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cf415-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="cf415-122"> (自動) </span><span class="sxs-lookup"><span data-stu-id="cf415-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="cf415-123">參數</span><span class="sxs-lookup"><span data-stu-id="cf415-123">PARAMETERS</span></span>

### <span data-ttu-id="cf415-124">-引數</span><span class="sxs-lookup"><span data-stu-id="cf415-124">-Argument</span></span>
<span data-ttu-id="cf415-125">指定腳本擴充功能傳遞至腳本的引數。</span><span class="sxs-lookup"><span data-stu-id="cf415-125">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="cf415-126">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="cf415-126">-ContainerName</span></span>
<span data-ttu-id="cf415-127">指定此 Cmdlet 儲存腳本的 Azure 儲存容器名稱。</span><span class="sxs-lookup"><span data-stu-id="cf415-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf415-128">-DefaultProfile</span></span>
<span data-ttu-id="cf415-129">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf415-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf415-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cf415-130">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-131">-FileName</span><span class="sxs-lookup"><span data-stu-id="cf415-131">-FileName</span></span>
<span data-ttu-id="cf415-132">指定指令檔名。</span><span class="sxs-lookup"><span data-stu-id="cf415-132">Specifies the name of the script file.</span></span> <span data-ttu-id="cf415-133">如果檔案是儲存在 Azure Blob 儲存體中，檔案名值會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cf415-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="cf415-134">儲存在 Azure 檔案儲存空間的檔案名不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cf415-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="cf415-135">-FileUri</span></span>
<span data-ttu-id="cf415-136">指定腳本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="cf415-136">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithFileUriParameterSet, ByResourceIdWithFileUriParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="cf415-137">-ForceRerun</span></span>
<span data-ttu-id="cf415-138">表示此 Cmdlet 強制在虛擬機器上重新進行相同的擴充功能組配置，而不需要卸載並重新安裝擴充功能。</span><span class="sxs-lookup"><span data-stu-id="cf415-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="cf415-139">該值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="cf415-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="cf415-140">如果未變更 forceUpdateTag，處理常式仍然會使用公用或受保護的設定更新。</span><span class="sxs-lookup"><span data-stu-id="cf415-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="cf415-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf415-141">-InputObject</span></span>
<span data-ttu-id="cf415-142">VM 擴充物件。</span><span class="sxs-lookup"><span data-stu-id="cf415-142">VM extension object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext
Parameter Sets: ByInputObjectWithContainerAndFileNamesParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-143">-位置</span><span class="sxs-lookup"><span data-stu-id="cf415-143">-Location</span></span>
<span data-ttu-id="cf415-144">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="cf415-144">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="cf415-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf415-145">-Name</span></span>
<span data-ttu-id="cf415-146">指定自訂腳本副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf415-146">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cf415-147">-NoWait</span></span>
<span data-ttu-id="cf415-148">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="cf415-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="cf415-149">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="cf415-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cf415-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf415-150">-ResourceGroupName</span></span>
<span data-ttu-id="cf415-151">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="cf415-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf415-152">-ResourceId</span></span>
<span data-ttu-id="cf415-153">VM 擴充功能 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="cf415-153">VM extension ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdWithContainerAndFileNamesParameterSet, ByResourceIdWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-154">-執行</span><span class="sxs-lookup"><span data-stu-id="cf415-154">-Run</span></span>
<span data-ttu-id="cf415-155">指定執行腳本時所使用的命令。</span><span class="sxs-lookup"><span data-stu-id="cf415-155">Specifies the command to use that runs your script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-156">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="cf415-156">-SecureExecution</span></span>
<span data-ttu-id="cf415-157">表示此 Cmdlet 會確定 *執行* 參數的值並未在伺服器上記錄，或是使用 GET 擴充 API 返回給使用者。</span><span class="sxs-lookup"><span data-stu-id="cf415-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="cf415-158">Run *值* 可能包含要安全地傳遞到腳本檔案的機密或密碼。</span><span class="sxs-lookup"><span data-stu-id="cf415-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cf415-159">-StorageAccountKey</span></span>
<span data-ttu-id="cf415-160">指定 Azure 儲存容器的金鑰。</span><span class="sxs-lookup"><span data-stu-id="cf415-160">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cf415-161">-StorageAccountName</span></span>
<span data-ttu-id="cf415-162">指定此 Cmdlet 儲存腳本的 Azure 儲存帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cf415-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-163">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="cf415-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="cf415-164">指定儲存端點尾碼。</span><span class="sxs-lookup"><span data-stu-id="cf415-164">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cf415-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="cf415-166">指定要用於此虛擬機器的擴充功能版本。</span><span class="sxs-lookup"><span data-stu-id="cf415-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="cf415-167">若要取得版本，請執行 Get-AzVMExtensionImage Cmdlet，其值為 Microsoft.Compute for *PublisherName* 參數，CustomScriptExtension 為 *Type* 參數。</span><span class="sxs-lookup"><span data-stu-id="cf415-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="cf415-168">-VMName</span></span>
<span data-ttu-id="cf415-169">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf415-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="cf415-170">此 Cmdlet 會新增此參數指定之虛擬機器的自訂腳本擴充功能。</span><span class="sxs-lookup"><span data-stu-id="cf415-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="cf415-171">-VMObject</span></span>
<span data-ttu-id="cf415-172">VM 物件。</span><span class="sxs-lookup"><span data-stu-id="cf415-172">VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-173">-確認</span><span class="sxs-lookup"><span data-stu-id="cf415-173">-Confirm</span></span>
<span data-ttu-id="cf415-174">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cf415-174">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf415-175">-WhatIf</span></span>
<span data-ttu-id="cf415-176">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf415-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf415-177">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf415-177">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf415-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf415-178">CommonParameters</span></span>
<span data-ttu-id="cf415-179">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cf415-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf415-180">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf415-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf415-181">輸入</span><span class="sxs-lookup"><span data-stu-id="cf415-181">INPUTS</span></span>

### <span data-ttu-id="cf415-182">System.String</span><span class="sxs-lookup"><span data-stu-id="cf415-182">System.String</span></span>

### <span data-ttu-id="cf415-183">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cf415-183">System.String[]</span></span>

### <span data-ttu-id="cf415-184">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cf415-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cf415-185">輸出</span><span class="sxs-lookup"><span data-stu-id="cf415-185">OUTPUTS</span></span>

### <span data-ttu-id="cf415-186">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cf415-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cf415-187">筆記</span><span class="sxs-lookup"><span data-stu-id="cf415-187">NOTES</span></span>

## <span data-ttu-id="cf415-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf415-188">RELATED LINKS</span></span>

[<span data-ttu-id="cf415-189">Get-AzTOMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cf415-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="cf415-190">Remove-AzTOMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cf415-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


