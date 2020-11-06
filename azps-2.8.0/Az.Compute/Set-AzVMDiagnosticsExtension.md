---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: ed3215d6ae5b4e6386dc1ee9fce951f8b036d39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613156"
---
# <span data-ttu-id="d8281-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d8281-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="d8281-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8281-102">SYNOPSIS</span></span>
<span data-ttu-id="d8281-103">在虛擬機器上配置 Azure diagnostics 延伸。</span><span class="sxs-lookup"><span data-stu-id="d8281-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d8281-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8281-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8281-105">說明</span><span class="sxs-lookup"><span data-stu-id="d8281-105">DESCRIPTION</span></span>
<span data-ttu-id="d8281-106">AzVMDiagnosticsExtension Cmdlet 會 **設定** 虛擬機器上的 Azure diagnostics 延伸。</span><span class="sxs-lookup"><span data-stu-id="d8281-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d8281-107">示例</span><span class="sxs-lookup"><span data-stu-id="d8281-107">EXAMPLES</span></span>

### <span data-ttu-id="d8281-108">範例1：使用在診斷設定檔中指定的儲存空間帳戶來啟用診斷</span><span class="sxs-lookup"><span data-stu-id="d8281-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="d8281-109">這個命令使用診斷設定檔來啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="d8281-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="d8281-110">檔案 diagnostics_publicconfig.xml 包含診斷延伸的公用 XML 配置，包括要傳送診斷資料之儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8281-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="d8281-111">診斷儲存空間帳戶必須與虛擬機器在同一個訂閱中。</span><span class="sxs-lookup"><span data-stu-id="d8281-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="d8281-112">範例2：使用儲存空間帳戶名稱啟用診斷</span><span class="sxs-lookup"><span data-stu-id="d8281-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="d8281-113">這個命令會使用儲存空間帳戶名稱來啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="d8281-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="d8281-114">如果診斷設定未指定儲存空間帳戶名稱，或您想要覆寫設定檔中指定的診斷儲存空間帳戶名稱，請使用 *StorageAccountName* 參數。</span><span class="sxs-lookup"><span data-stu-id="d8281-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="d8281-115">診斷儲存空間帳戶必須與虛擬機器在同一個訂閱中。</span><span class="sxs-lookup"><span data-stu-id="d8281-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="d8281-116">範例3：使用儲存空間帳戶名稱和金鑰啟用診斷</span><span class="sxs-lookup"><span data-stu-id="d8281-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="d8281-117">這個命令會使用儲存空間帳戶名稱和金鑰來啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="d8281-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="d8281-118">如果診斷儲存空間帳戶與虛擬機器的訂閱不同，則請明確指定其名稱和金鑰，以啟用將診斷資料傳送至該儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="d8281-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="d8281-119">參數</span><span class="sxs-lookup"><span data-stu-id="d8281-119">PARAMETERS</span></span>

### <span data-ttu-id="d8281-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d8281-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d8281-121">指示此 Cmdlet 是否允許 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="d8281-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="d8281-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8281-122">-DefaultProfile</span></span>
<span data-ttu-id="d8281-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8281-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8281-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="d8281-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="d8281-125">指定設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="d8281-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8281-126">-位置</span><span class="sxs-lookup"><span data-stu-id="d8281-126">-Location</span></span>
<span data-ttu-id="d8281-127">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="d8281-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d8281-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8281-128">-Name</span></span>
<span data-ttu-id="d8281-129">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8281-129">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8281-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d8281-130">-NoWait</span></span>
<span data-ttu-id="d8281-131">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="d8281-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d8281-132">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="d8281-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d8281-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8281-133">-ResourceGroupName</span></span>
<span data-ttu-id="d8281-134">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8281-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8281-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8281-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="d8281-136">指定 [儲存空間帳戶] 端點。</span><span class="sxs-lookup"><span data-stu-id="d8281-136">Specifies the storage account endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8281-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d8281-137">-StorageAccountKey</span></span>
<span data-ttu-id="d8281-138">指定儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="d8281-138">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="d8281-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d8281-139">-StorageAccountName</span></span>
<span data-ttu-id="d8281-140">指定儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d8281-140">Specifies the storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8281-141">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="d8281-141">-StorageContext</span></span>
<span data-ttu-id="d8281-142">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="d8281-142">Specifies the Azure storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8281-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d8281-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="d8281-144">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="d8281-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d8281-145">若要取得版本，請使用 Microsoft 的值來執行 Get-AzVMExtensionImage Cmdlet。針對 *PublisherName* 參數和 VMAccessAgent （針對 *Type* 參數）進行計算。</span><span class="sxs-lookup"><span data-stu-id="d8281-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8281-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="d8281-146">-VMName</span></span>
<span data-ttu-id="d8281-147">指定此 Cmdlet 作用中的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="d8281-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8281-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8281-148">CommonParameters</span></span>
<span data-ttu-id="d8281-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8281-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8281-150">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d8281-150">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8281-151">輸入</span><span class="sxs-lookup"><span data-stu-id="d8281-151">INPUTS</span></span>

### <span data-ttu-id="d8281-152">System.object</span><span class="sxs-lookup"><span data-stu-id="d8281-152">System.String</span></span>

### <span data-ttu-id="d8281-153">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="d8281-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="d8281-154">System.object</span><span class="sxs-lookup"><span data-stu-id="d8281-154">System.Boolean</span></span>

## <span data-ttu-id="d8281-155">輸出</span><span class="sxs-lookup"><span data-stu-id="d8281-155">OUTPUTS</span></span>

### <span data-ttu-id="d8281-156">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="d8281-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d8281-157">筆記</span><span class="sxs-lookup"><span data-stu-id="d8281-157">NOTES</span></span>

## <span data-ttu-id="d8281-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8281-158">RELATED LINKS</span></span>

[<span data-ttu-id="d8281-159">AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d8281-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="d8281-160">AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d8281-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="d8281-161">移除-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d8281-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


