---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: f32b49e28f34b676c4154793ac37989b58b0c917
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801378"
---
# <span data-ttu-id="04c5e-101">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="04c5e-101">Set-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="04c5e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="04c5e-103">在虛擬機器上配置 Azure diagnostics 延伸。</span><span class="sxs-lookup"><span data-stu-id="04c5e-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04c5e-104">句法</span><span class="sxs-lookup"><span data-stu-id="04c5e-104">SYNTAX</span></span>

```
Set-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04c5e-105">說明</span><span class="sxs-lookup"><span data-stu-id="04c5e-105">DESCRIPTION</span></span>
<span data-ttu-id="04c5e-106">AzureRmVMDiagnosticsExtension Cmdlet 會 **設定** 虛擬機器上的 Azure diagnostics 延伸。</span><span class="sxs-lookup"><span data-stu-id="04c5e-106">The **Set-AzureRmVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="04c5e-107">示例</span><span class="sxs-lookup"><span data-stu-id="04c5e-107">EXAMPLES</span></span>

### <span data-ttu-id="04c5e-108">範例1：使用在診斷設定檔中指定的儲存空間帳戶來啟用診斷</span><span class="sxs-lookup"><span data-stu-id="04c5e-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="04c5e-109">這個命令使用診斷設定檔來啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="04c5e-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="04c5e-110">檔案 diagnostics_publicconfig.xml 包含診斷延伸的公用 XML 配置，包括要傳送診斷資料之儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c5e-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="04c5e-111">診斷儲存空間帳戶必須與虛擬機器在同一個訂閱中。</span><span class="sxs-lookup"><span data-stu-id="04c5e-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="04c5e-112">範例2：使用儲存空間帳戶名稱啟用診斷</span><span class="sxs-lookup"><span data-stu-id="04c5e-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="04c5e-113">這個命令會使用儲存空間帳戶名稱來啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="04c5e-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="04c5e-114">如果診斷設定未指定儲存空間帳戶名稱，或您想要覆寫設定檔中指定的診斷儲存空間帳戶名稱，請使用 *StorageAccountName* 參數。</span><span class="sxs-lookup"><span data-stu-id="04c5e-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="04c5e-115">診斷儲存空間帳戶必須與虛擬機器在同一個訂閱中。</span><span class="sxs-lookup"><span data-stu-id="04c5e-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="04c5e-116">範例3：使用儲存空間帳戶名稱和金鑰啟用診斷</span><span class="sxs-lookup"><span data-stu-id="04c5e-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="04c5e-117">這個命令會使用儲存空間帳戶名稱和金鑰來啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="04c5e-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="04c5e-118">如果診斷儲存空間帳戶與虛擬機器的訂閱不同，則請明確指定其名稱和金鑰，以啟用將診斷資料傳送至該儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="04c5e-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="04c5e-119">參數</span><span class="sxs-lookup"><span data-stu-id="04c5e-119">PARAMETERS</span></span>

### <span data-ttu-id="04c5e-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="04c5e-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="04c5e-121">指示此 Cmdlet 是否允許 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="04c5e-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="04c5e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c5e-122">-DefaultProfile</span></span>
<span data-ttu-id="04c5e-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04c5e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04c5e-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="04c5e-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="04c5e-125">指定設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="04c5e-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c5e-126">-位置</span><span class="sxs-lookup"><span data-stu-id="04c5e-126">-Location</span></span>
<span data-ttu-id="04c5e-127">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="04c5e-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="04c5e-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="04c5e-128">-Name</span></span>
<span data-ttu-id="04c5e-129">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c5e-129">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04c5e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04c5e-130">-ResourceGroupName</span></span>
<span data-ttu-id="04c5e-131">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c5e-131">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="04c5e-132">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="04c5e-132">-StorageAccountEndpoint</span></span>
<span data-ttu-id="04c5e-133">指定 [儲存空間帳戶] 端點。</span><span class="sxs-lookup"><span data-stu-id="04c5e-133">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04c5e-134">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="04c5e-134">-StorageAccountKey</span></span>
<span data-ttu-id="04c5e-135">指定儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="04c5e-135">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="04c5e-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="04c5e-136">-StorageAccountName</span></span>
<span data-ttu-id="04c5e-137">指定儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="04c5e-137">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04c5e-138">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="04c5e-138">-StorageContext</span></span>
<span data-ttu-id="04c5e-139">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="04c5e-139">Specifies the Azure storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04c5e-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="04c5e-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="04c5e-141">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="04c5e-141">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="04c5e-142">若要取得版本，請使用 Microsoft 的值來執行 Get-AzureRmVMExtensionImage Cmdlet。針對 *PublisherName* 參數和 VMAccessAgent （針對 *Type* 參數）進行計算。</span><span class="sxs-lookup"><span data-stu-id="04c5e-142">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04c5e-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="04c5e-143">-VMName</span></span>
<span data-ttu-id="04c5e-144">指定此 Cmdlet 作用中的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="04c5e-144">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="04c5e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c5e-145">CommonParameters</span></span>
<span data-ttu-id="04c5e-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04c5e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c5e-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04c5e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c5e-148">輸入</span><span class="sxs-lookup"><span data-stu-id="04c5e-148">INPUTS</span></span>

### <span data-ttu-id="04c5e-149">所有</span><span class="sxs-lookup"><span data-stu-id="04c5e-149">None</span></span>
<span data-ttu-id="04c5e-150">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="04c5e-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04c5e-151">輸出</span><span class="sxs-lookup"><span data-stu-id="04c5e-151">OUTPUTS</span></span>

### <span data-ttu-id="04c5e-152">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="04c5e-152">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="04c5e-153">筆記</span><span class="sxs-lookup"><span data-stu-id="04c5e-153">NOTES</span></span>

## <span data-ttu-id="04c5e-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="04c5e-154">RELATED LINKS</span></span>

[<span data-ttu-id="04c5e-155">AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="04c5e-155">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="04c5e-156">AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="04c5e-156">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="04c5e-157">移除-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="04c5e-157">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)


