---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 69b6dec11f0135803320bb7b58bdb8362aaee26e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449696"
---
# <span data-ttu-id="2016b-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2016b-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="2016b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2016b-102">SYNOPSIS</span></span>
<span data-ttu-id="2016b-103">新增自訂腳本延伸至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2016b-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="2016b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2016b-104">SYNTAX</span></span>

### <span data-ttu-id="2016b-105">ByNameWithContainerAndFileNamesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2016b-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2016b-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="2016b-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2016b-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="2016b-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2016b-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="2016b-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2016b-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="2016b-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2016b-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="2016b-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2016b-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="2016b-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2016b-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="2016b-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2016b-113">說明</span><span class="sxs-lookup"><span data-stu-id="2016b-113">DESCRIPTION</span></span>
<span data-ttu-id="2016b-114">**AzVMCustomScriptExtension** Cmdlet 會將自訂腳本虛擬機器延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2016b-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="2016b-115">此延伸功能可讓您在虛擬機器上執行自己的腳本。</span><span class="sxs-lookup"><span data-stu-id="2016b-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="2016b-116">示例</span><span class="sxs-lookup"><span data-stu-id="2016b-116">EXAMPLES</span></span>

### <span data-ttu-id="2016b-117">範例1：新增自訂腳本</span><span class="sxs-lookup"><span data-stu-id="2016b-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="2016b-118">這個命令會將自訂腳本新增到名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2016b-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="2016b-119">腳本檔案是 contososcript.exe 的。</span><span class="sxs-lookup"><span data-stu-id="2016b-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="2016b-120">範例2</span><span class="sxs-lookup"><span data-stu-id="2016b-120">Example 2</span></span>

<span data-ttu-id="2016b-121">新增自訂腳本延伸至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2016b-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="2016b-122"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="2016b-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="2016b-123">參數</span><span class="sxs-lookup"><span data-stu-id="2016b-123">PARAMETERS</span></span>

### <span data-ttu-id="2016b-124">-引數</span><span class="sxs-lookup"><span data-stu-id="2016b-124">-Argument</span></span>
<span data-ttu-id="2016b-125">指定腳本延伸傳給腳本的引數。</span><span class="sxs-lookup"><span data-stu-id="2016b-125">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="2016b-126">-容器</span><span class="sxs-lookup"><span data-stu-id="2016b-126">-ContainerName</span></span>
<span data-ttu-id="2016b-127">指定此 Cmdlet 儲存腳本的 Azure 儲存體容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2016b-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="2016b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2016b-128">-DefaultProfile</span></span>
<span data-ttu-id="2016b-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2016b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2016b-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2016b-130">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="2016b-131">-FileName</span><span class="sxs-lookup"><span data-stu-id="2016b-131">-FileName</span></span>
<span data-ttu-id="2016b-132">指定腳本檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="2016b-132">Specifies the name of the script file.</span></span> <span data-ttu-id="2016b-133">如果檔案儲存在 Azure Blob 儲存空間中，則 [檔案名] 值會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2016b-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="2016b-134">儲存在 Azure 檔案儲存空間中之檔案的檔案名不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2016b-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

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

### <span data-ttu-id="2016b-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="2016b-135">-FileUri</span></span>
<span data-ttu-id="2016b-136">指定腳本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="2016b-136">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="2016b-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="2016b-137">-ForceRerun</span></span>
<span data-ttu-id="2016b-138">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="2016b-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="2016b-139">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="2016b-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="2016b-140">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="2016b-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="2016b-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2016b-141">-InputObject</span></span>
<span data-ttu-id="2016b-142">VM 延伸物件。</span><span class="sxs-lookup"><span data-stu-id="2016b-142">VM extension object.</span></span>

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

### <span data-ttu-id="2016b-143">-位置</span><span class="sxs-lookup"><span data-stu-id="2016b-143">-Location</span></span>
<span data-ttu-id="2016b-144">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="2016b-144">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="2016b-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="2016b-145">-Name</span></span>
<span data-ttu-id="2016b-146">指定自訂腳本副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="2016b-146">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="2016b-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2016b-147">-NoWait</span></span>
<span data-ttu-id="2016b-148">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="2016b-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2016b-149">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="2016b-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2016b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2016b-150">-ResourceGroupName</span></span>
<span data-ttu-id="2016b-151">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2016b-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2016b-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2016b-152">-ResourceId</span></span>
<span data-ttu-id="2016b-153">VM 延伸 Id。</span><span class="sxs-lookup"><span data-stu-id="2016b-153">VM extension ResourceID.</span></span>

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

### <span data-ttu-id="2016b-154">-執行</span><span class="sxs-lookup"><span data-stu-id="2016b-154">-Run</span></span>
<span data-ttu-id="2016b-155">指定要使用的命令來執行您的腳本。</span><span class="sxs-lookup"><span data-stu-id="2016b-155">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="2016b-156">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="2016b-156">-SecureExecution</span></span>
<span data-ttu-id="2016b-157">表示此 Cmdlet 會確保不會在伺服器上記錄 *Run* 參數的值，或使用 [取得擴充 API] 傳回給使用者。</span><span class="sxs-lookup"><span data-stu-id="2016b-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="2016b-158">*Run* 的值可能包含要安全地傳遞到腳本檔案的機密或密碼。</span><span class="sxs-lookup"><span data-stu-id="2016b-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="2016b-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2016b-159">-StorageAccountKey</span></span>
<span data-ttu-id="2016b-160">指定 Azure 存儲容器的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2016b-160">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="2016b-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2016b-161">-StorageAccountName</span></span>
<span data-ttu-id="2016b-162">指定此 Cmdlet 儲存腳本的 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2016b-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="2016b-163">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2016b-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="2016b-164">指定儲存端點尾碼。</span><span class="sxs-lookup"><span data-stu-id="2016b-164">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="2016b-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2016b-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="2016b-166">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="2016b-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="2016b-167">若要取得版本，請使用 Microsoft 的值來執行 Get-AzVMExtensionImage Cmdlet。針對 *PublisherName* 參數和 CustomScriptExtension （針對 *Type* 參數）進行計算。</span><span class="sxs-lookup"><span data-stu-id="2016b-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="2016b-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="2016b-168">-VMName</span></span>
<span data-ttu-id="2016b-169">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2016b-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2016b-170">這個 Cmdlet 會新增此參數指定之虛擬機器的自訂腳本副檔名。</span><span class="sxs-lookup"><span data-stu-id="2016b-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2016b-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="2016b-171">-VMObject</span></span>
<span data-ttu-id="2016b-172">VM 物件。</span><span class="sxs-lookup"><span data-stu-id="2016b-172">VM object.</span></span>

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

### <span data-ttu-id="2016b-173">-確認</span><span class="sxs-lookup"><span data-stu-id="2016b-173">-Confirm</span></span>
<span data-ttu-id="2016b-174">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2016b-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2016b-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2016b-175">-WhatIf</span></span>
<span data-ttu-id="2016b-176">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2016b-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2016b-177">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2016b-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2016b-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2016b-178">CommonParameters</span></span>
<span data-ttu-id="2016b-179">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2016b-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2016b-180">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2016b-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2016b-181">輸入</span><span class="sxs-lookup"><span data-stu-id="2016b-181">INPUTS</span></span>

### <span data-ttu-id="2016b-182">System.object</span><span class="sxs-lookup"><span data-stu-id="2016b-182">System.String</span></span>

### <span data-ttu-id="2016b-183">System.object []</span><span class="sxs-lookup"><span data-stu-id="2016b-183">System.String[]</span></span>

### <span data-ttu-id="2016b-184">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="2016b-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2016b-185">輸出</span><span class="sxs-lookup"><span data-stu-id="2016b-185">OUTPUTS</span></span>

### <span data-ttu-id="2016b-186">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="2016b-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2016b-187">筆記</span><span class="sxs-lookup"><span data-stu-id="2016b-187">NOTES</span></span>

## <span data-ttu-id="2016b-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="2016b-188">RELATED LINKS</span></span>

[<span data-ttu-id="2016b-189">AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2016b-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="2016b-190">移除-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2016b-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


