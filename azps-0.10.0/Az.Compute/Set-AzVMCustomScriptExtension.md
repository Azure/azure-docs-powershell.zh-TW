---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 6fe34ae33ed70cebe4c8f76beb235e6fa7445fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795886"
---
# <span data-ttu-id="2380e-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2380e-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="2380e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2380e-102">SYNOPSIS</span></span>
<span data-ttu-id="2380e-103">新增自訂腳本延伸至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2380e-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="2380e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2380e-104">SYNTAX</span></span>

### <span data-ttu-id="2380e-105">SetCustomScriptExtensionByContainerAndFileNames (預設) </span><span class="sxs-lookup"><span data-stu-id="2380e-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2380e-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="2380e-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2380e-107">說明</span><span class="sxs-lookup"><span data-stu-id="2380e-107">DESCRIPTION</span></span>
<span data-ttu-id="2380e-108">**AzVMCustomScriptExtension** Cmdlet 會將自訂腳本虛擬機器延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2380e-108">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="2380e-109">此延伸功能可讓您在虛擬機器上執行自己的腳本。</span><span class="sxs-lookup"><span data-stu-id="2380e-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="2380e-110">示例</span><span class="sxs-lookup"><span data-stu-id="2380e-110">EXAMPLES</span></span>

### <span data-ttu-id="2380e-111">範例1：新增自訂腳本</span><span class="sxs-lookup"><span data-stu-id="2380e-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="2380e-112">這個命令會將自訂腳本新增到名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2380e-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="2380e-113">腳本檔案是 contososcript.exe 的。</span><span class="sxs-lookup"><span data-stu-id="2380e-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="2380e-114">參數</span><span class="sxs-lookup"><span data-stu-id="2380e-114">PARAMETERS</span></span>

### <span data-ttu-id="2380e-115">-引數</span><span class="sxs-lookup"><span data-stu-id="2380e-115">-Argument</span></span>
<span data-ttu-id="2380e-116">指定腳本延伸傳給腳本的引數。</span><span class="sxs-lookup"><span data-stu-id="2380e-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="2380e-117">-容器</span><span class="sxs-lookup"><span data-stu-id="2380e-117">-ContainerName</span></span>
<span data-ttu-id="2380e-118">指定此 Cmdlet 儲存腳本的 Azure 儲存體容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2380e-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2380e-119">-DefaultProfile</span></span>
<span data-ttu-id="2380e-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2380e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2380e-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2380e-121">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="2380e-122">-FileName</span></span>
<span data-ttu-id="2380e-123">指定腳本檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="2380e-123">Specifies the name of the script file.</span></span> <span data-ttu-id="2380e-124">如果檔案是儲存在 Azure Blob 儲存空間中，則 [檔案名] 值會是 case senstive。</span><span class="sxs-lookup"><span data-stu-id="2380e-124">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="2380e-125">儲存在 Azure 檔案儲存空間中之檔案的檔案名不是大小寫的 senstive。</span><span class="sxs-lookup"><span data-stu-id="2380e-125">File names of files stored in Azure File storage are not case-senstive.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-126">-FileUri</span><span class="sxs-lookup"><span data-stu-id="2380e-126">-FileUri</span></span>
<span data-ttu-id="2380e-127">指定腳本檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="2380e-127">Specifies the URI of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="2380e-128">-ForceRerun</span></span>
<span data-ttu-id="2380e-129">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="2380e-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="2380e-130">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="2380e-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="2380e-131">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="2380e-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="2380e-132">-位置</span><span class="sxs-lookup"><span data-stu-id="2380e-132">-Location</span></span>
<span data-ttu-id="2380e-133">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="2380e-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="2380e-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="2380e-134">-Name</span></span>
<span data-ttu-id="2380e-135">指定自訂腳本副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="2380e-135">Specifies the name of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2380e-136">-ResourceGroupName</span></span>
<span data-ttu-id="2380e-137">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2380e-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-138">-執行</span><span class="sxs-lookup"><span data-stu-id="2380e-138">-Run</span></span>
<span data-ttu-id="2380e-139">指定要使用的命令來執行您的腳本。</span><span class="sxs-lookup"><span data-stu-id="2380e-139">Specifies the command to use that runs your script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-140">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="2380e-140">-SecureExecution</span></span>
<span data-ttu-id="2380e-141">表示此 Cmdlet 會確保不會在伺服器上記錄 *Run* 參數的值，或使用 [取得擴充 API] 傳回給使用者。</span><span class="sxs-lookup"><span data-stu-id="2380e-141">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="2380e-142">*Run* 的值可能包含要安全地傳遞到腳本檔案的機密或密碼。</span><span class="sxs-lookup"><span data-stu-id="2380e-142">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2380e-143">-StorageAccountKey</span></span>
<span data-ttu-id="2380e-144">指定 Azure 存儲容器的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2380e-144">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2380e-145">-StorageAccountName</span></span>
<span data-ttu-id="2380e-146">指定此 Cmdlet 儲存腳本的 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2380e-146">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-147">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2380e-147">-StorageEndpointSuffix</span></span>
<span data-ttu-id="2380e-148">指定儲存端點尾碼。</span><span class="sxs-lookup"><span data-stu-id="2380e-148">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2380e-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="2380e-150">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="2380e-150">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="2380e-151">若要取得版本，請使用 Microsoft 的值來執行 Get-AzVMExtensionImage Cmdlet。針對 *PublisherName* 參數和 VMAccessAgent （針對 *Type* 參數）進行計算。</span><span class="sxs-lookup"><span data-stu-id="2380e-151">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-152">-VMName</span><span class="sxs-lookup"><span data-stu-id="2380e-152">-VMName</span></span>
<span data-ttu-id="2380e-153">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2380e-153">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2380e-154">這個 Cmdlet 會新增此參數指定之虛擬機器的自訂腳本副檔名。</span><span class="sxs-lookup"><span data-stu-id="2380e-154">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-155">-確認</span><span class="sxs-lookup"><span data-stu-id="2380e-155">-Confirm</span></span>
<span data-ttu-id="2380e-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2380e-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2380e-157">-WhatIf</span></span>
<span data-ttu-id="2380e-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2380e-158">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2380e-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2380e-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2380e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2380e-160">CommonParameters</span></span>
<span data-ttu-id="2380e-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2380e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2380e-162">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2380e-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2380e-163">輸入</span><span class="sxs-lookup"><span data-stu-id="2380e-163">INPUTS</span></span>

### <span data-ttu-id="2380e-164">所有</span><span class="sxs-lookup"><span data-stu-id="2380e-164">None</span></span>
<span data-ttu-id="2380e-165">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2380e-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2380e-166">輸出</span><span class="sxs-lookup"><span data-stu-id="2380e-166">OUTPUTS</span></span>

### <span data-ttu-id="2380e-167">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="2380e-167">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2380e-168">筆記</span><span class="sxs-lookup"><span data-stu-id="2380e-168">NOTES</span></span>

## <span data-ttu-id="2380e-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="2380e-169">RELATED LINKS</span></span>

[<span data-ttu-id="2380e-170">AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2380e-170">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="2380e-171">移除-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2380e-171">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


