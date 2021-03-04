---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9e33f3e956f7d1fee0d93eebf5e14fa0df460303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917345"
---
# <span data-ttu-id="977e3-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="977e3-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="977e3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="977e3-102">SYNOPSIS</span></span>
<span data-ttu-id="977e3-103">設定虛擬機器上的 Azure 診斷擴充功能。</span><span class="sxs-lookup"><span data-stu-id="977e3-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="977e3-104">語法</span><span class="sxs-lookup"><span data-stu-id="977e3-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="977e3-105">描述</span><span class="sxs-lookup"><span data-stu-id="977e3-105">DESCRIPTION</span></span>
<span data-ttu-id="977e3-106">**Set-Az VIRTUALDiagnosticsExtension** Cmdlet 會設定虛擬機器上的 Azure 診斷擴充功能。</span><span class="sxs-lookup"><span data-stu-id="977e3-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="977e3-107">例子</span><span class="sxs-lookup"><span data-stu-id="977e3-107">EXAMPLES</span></span>

### <span data-ttu-id="977e3-108">範例 1：使用診斷組設定檔中指定的儲存空間帳戶啟用診斷</span><span class="sxs-lookup"><span data-stu-id="977e3-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="977e3-109">此命令使用診斷設定檔啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="977e3-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="977e3-110">檔案diagnostics_publicconfig.xml包含診斷副檔名的公用 XML 組配置，包括要送出診斷資料的儲存帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="977e3-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="977e3-111">診斷儲存空間帳戶必須和虛擬機器在同一個訂閱中。</span><span class="sxs-lookup"><span data-stu-id="977e3-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="977e3-112">範例 2：使用儲存空間帳戶名稱啟用診斷</span><span class="sxs-lookup"><span data-stu-id="977e3-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="977e3-113">此命令會使用儲存空間帳戶名稱來啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="977e3-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="977e3-114">如果診斷設定未指定儲存帳戶名稱，或如果您想要覆蓋群組原則檔中指定的診斷儲存帳戶名稱，請使用 *StorageAccountName* 參數。</span><span class="sxs-lookup"><span data-stu-id="977e3-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="977e3-115">診斷儲存空間帳戶必須和虛擬機器在同一個訂閱中。</span><span class="sxs-lookup"><span data-stu-id="977e3-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="977e3-116">範例 3：使用儲存空間帳戶名稱和金鑰啟用診斷</span><span class="sxs-lookup"><span data-stu-id="977e3-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="977e3-117">此命令使用儲存空間帳戶名稱和金鑰來啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="977e3-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="977e3-118">如果診斷儲存帳戶的訂閱與虛擬機器不同，請明確指定其名稱和金鑰，以啟用將診斷資料傳送至該儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="977e3-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="977e3-119">參數</span><span class="sxs-lookup"><span data-stu-id="977e3-119">PARAMETERS</span></span>

### <span data-ttu-id="977e3-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="977e3-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="977e3-121">指出此 Cmdlet 是否允許 Azure 來賓代理程式自動更新擴充功能至較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="977e3-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="977e3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977e3-122">-DefaultProfile</span></span>
<span data-ttu-id="977e3-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="977e3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="977e3-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="977e3-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="977e3-125">指定群組原則案的路徑。</span><span class="sxs-lookup"><span data-stu-id="977e3-125">Specifies the path of the configuration file.</span></span>

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

### <span data-ttu-id="977e3-126">-位置</span><span class="sxs-lookup"><span data-stu-id="977e3-126">-Location</span></span>
<span data-ttu-id="977e3-127">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="977e3-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="977e3-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="977e3-128">-Name</span></span>
<span data-ttu-id="977e3-129">指定副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="977e3-129">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="977e3-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="977e3-130">-NoWait</span></span>
<span data-ttu-id="977e3-131">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="977e3-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="977e3-132">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="977e3-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="977e3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="977e3-133">-ResourceGroupName</span></span>
<span data-ttu-id="977e3-134">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="977e3-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="977e3-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="977e3-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="977e3-136">指定儲存帳戶端點。</span><span class="sxs-lookup"><span data-stu-id="977e3-136">Specifies the storage account endpoint.</span></span>

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

### <span data-ttu-id="977e3-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="977e3-137">-StorageAccountKey</span></span>
<span data-ttu-id="977e3-138">指定儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="977e3-138">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="977e3-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="977e3-139">-StorageAccountName</span></span>
<span data-ttu-id="977e3-140">指定儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="977e3-140">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="977e3-141">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="977e3-141">-StorageContext</span></span>
<span data-ttu-id="977e3-142">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="977e3-142">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="977e3-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="977e3-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="977e3-144">指定要用於此虛擬機器的擴充功能版本。</span><span class="sxs-lookup"><span data-stu-id="977e3-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="977e3-145">若要取得版本，請執行 Get-AzVMExtensionImage Cmdlet，其值為 Microsoft.Compute for *PublisherName* 參數，而 VMAccessAgent 為 *Type* 參數。</span><span class="sxs-lookup"><span data-stu-id="977e3-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="977e3-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="977e3-146">-VMName</span></span>
<span data-ttu-id="977e3-147">指定此 Cmdlet 操作之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="977e3-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="977e3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977e3-148">CommonParameters</span></span>
<span data-ttu-id="977e3-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="977e3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="977e3-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="977e3-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977e3-151">輸入</span><span class="sxs-lookup"><span data-stu-id="977e3-151">INPUTS</span></span>

### <span data-ttu-id="977e3-152">System.String</span><span class="sxs-lookup"><span data-stu-id="977e3-152">System.String</span></span>

### <span data-ttu-id="977e3-153">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="977e3-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="977e3-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="977e3-154">System.Boolean</span></span>

## <span data-ttu-id="977e3-155">輸出</span><span class="sxs-lookup"><span data-stu-id="977e3-155">OUTPUTS</span></span>

### <span data-ttu-id="977e3-156">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="977e3-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="977e3-157">筆記</span><span class="sxs-lookup"><span data-stu-id="977e3-157">NOTES</span></span>

## <span data-ttu-id="977e3-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="977e3-158">RELATED LINKS</span></span>

[<span data-ttu-id="977e3-159">Get-AzMSDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="977e3-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="977e3-160">Get-Az解說ExtensionImage</span><span class="sxs-lookup"><span data-stu-id="977e3-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="977e3-161">Remove-AzMSDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="977e3-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


