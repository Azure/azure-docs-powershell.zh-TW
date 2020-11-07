---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967401"
---
# <span data-ttu-id="a805a-101">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="a805a-101">Set-AzurePublicIP</span></span>

## <span data-ttu-id="a805a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a805a-102">SYNOPSIS</span></span>
<span data-ttu-id="a805a-103">新增公用 IP 至 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a805a-103">Adds a Public IP to an Azure virtual machine.</span></span>

## <span data-ttu-id="a805a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a805a-104">SYNTAX</span></span>

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a805a-105">說明</span><span class="sxs-lookup"><span data-stu-id="a805a-105">DESCRIPTION</span></span>
<span data-ttu-id="a805a-106">**AzurePublicIP** Cmdlet 會將公用 IP 新增至 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a805a-106">The **Set-AzurePublicIP** cmdlet adds a Public IP to an Azure virtual machine.</span></span>
<span data-ttu-id="a805a-107">如果您在現有的虛擬機器上執行這個 Cmdlet，請更新虛擬機器以實現您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="a805a-107">If you run this cmdlet for an existing virtual machine, update the virtual machine to implement your changes.</span></span>
<span data-ttu-id="a805a-108">您可以指定網功能變數名稱稱標籤，為公用 IP 建立對應的 DNS 專案。</span><span class="sxs-lookup"><span data-stu-id="a805a-108">You can specify a domain name label to create a corresponding DNS entry for the public IP.</span></span>

## <span data-ttu-id="a805a-109">示例</span><span class="sxs-lookup"><span data-stu-id="a805a-109">EXAMPLES</span></span>

### <span data-ttu-id="a805a-110">範例1：在現有的虛擬機器中新增公用 IP</span><span class="sxs-lookup"><span data-stu-id="a805a-110">Example 1: Add a Public IP to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

<span data-ttu-id="a805a-111">這個命令會透過使用 **FTPInstance Cmdlet，** 在名為 FTPInAzure 的服務中，取得名為的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a805a-111">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="a805a-112">命令會使用管線運算子，將該虛擬機器傳至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a805a-112">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a805a-113">目前的 Cmdlet 會新增公用 IP 名稱 ftpip。</span><span class="sxs-lookup"><span data-stu-id="a805a-113">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="a805a-114">該命令會將虛擬機器傳到由 **add-azurevm** Cmdlet （可實現您的變更）。</span><span class="sxs-lookup"><span data-stu-id="a805a-114">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="a805a-115">範例2：將公用 IP 新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a805a-115">Example 2: Add a Public IP to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="a805a-116">這個命令會使用 **AzureVMConfig** Cmdlet 來建立虛擬機器設定物件。</span><span class="sxs-lookup"><span data-stu-id="a805a-116">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="a805a-117">該命令會將該物件傳遞至 **AzureProvisioningConfig** Cmdlet，這會提供額外的配置。</span><span class="sxs-lookup"><span data-stu-id="a805a-117">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet, which provides additional configuration.</span></span>
<span data-ttu-id="a805a-118">目前的 Cmdlet 會新增公用 IP 名稱 ftpip。</span><span class="sxs-lookup"><span data-stu-id="a805a-118">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="a805a-119">該命令會將設定傳遞到 **新的 add-azurevm** Cmdlet，這會建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a805a-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="a805a-120">範例3：新增公用 IP 與標籤至現有的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a805a-120">Example 3: Add a Public IP and label to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

<span data-ttu-id="a805a-121">這個命令會透過使用 **FTPInstance Cmdlet，** 在名為 FTPInAzure 的服務中，取得名為的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a805a-121">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="a805a-122">命令會使用管線運算子，將該虛擬機器傳至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a805a-122">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a805a-123">目前的 Cmdlet 會新增公用 IP 名稱 ftpip 和標籤 ipname。</span><span class="sxs-lookup"><span data-stu-id="a805a-123">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="a805a-124">此命令會更新實現變更的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a805a-124">The command updates the virtual machine, which implements your changes.</span></span>

### <span data-ttu-id="a805a-125">範例4：將公用 IP 和標籤新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a805a-125">Example 4: Add a Public IP and label to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="a805a-126">這個命令會建立虛擬機器設定物件，然後將該物件傳遞給 **AzureProvisioningConfig** ，以提供額外的配置。</span><span class="sxs-lookup"><span data-stu-id="a805a-126">This command creates a virtual machine configuration object, and then passes that object to **Add-AzureProvisioningConfig** , which provides additional configuration.</span></span>
<span data-ttu-id="a805a-127">目前的 Cmdlet 會新增公用 IP 名稱 ftpip 和標籤 ipname。</span><span class="sxs-lookup"><span data-stu-id="a805a-127">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="a805a-128">命令會建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a805a-128">The command creates the virtual machine.</span></span>

## <span data-ttu-id="a805a-129">參數</span><span class="sxs-lookup"><span data-stu-id="a805a-129">PARAMETERS</span></span>

### <span data-ttu-id="a805a-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="a805a-130">-DomainNameLabel</span></span>
<span data-ttu-id="a805a-131">指定用於公用 IP 位址之對應 DNS 專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="a805a-131">Specifies the name to use for a corresponding DNS entry for the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a805a-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a805a-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a805a-133">指定 TCP 空閒超時時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="a805a-133">Specifies the TCP idle time-out period in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a805a-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a805a-134">-InformationAction</span></span>
<span data-ttu-id="a805a-135">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="a805a-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a805a-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a805a-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a805a-137">持續</span><span class="sxs-lookup"><span data-stu-id="a805a-137">Continue</span></span>
- <span data-ttu-id="a805a-138">理會</span><span class="sxs-lookup"><span data-stu-id="a805a-138">Ignore</span></span>
- <span data-ttu-id="a805a-139">看</span><span class="sxs-lookup"><span data-stu-id="a805a-139">Inquire</span></span>
- <span data-ttu-id="a805a-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a805a-140">SilentlyContinue</span></span>
- <span data-ttu-id="a805a-141">停止</span><span class="sxs-lookup"><span data-stu-id="a805a-141">Stop</span></span>
- <span data-ttu-id="a805a-142">封存</span><span class="sxs-lookup"><span data-stu-id="a805a-142">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a805a-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a805a-143">-InformationVariable</span></span>
<span data-ttu-id="a805a-144">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="a805a-144">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a805a-145">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a805a-145">-Profile</span></span>
<span data-ttu-id="a805a-146">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a805a-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a805a-147">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a805a-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a805a-148">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="a805a-148">-PublicIPName</span></span>
<span data-ttu-id="a805a-149">指定公用 IP 名稱。</span><span class="sxs-lookup"><span data-stu-id="a805a-149">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a805a-150">-VM</span><span class="sxs-lookup"><span data-stu-id="a805a-150">-VM</span></span>
<span data-ttu-id="a805a-151">指定此 Cmdlet 新增公用 IP 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a805a-151">Specifies the virtual machine to which this cmdlet adds Public IP.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a805a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a805a-152">CommonParameters</span></span>
<span data-ttu-id="a805a-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a805a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a805a-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a805a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a805a-155">輸入</span><span class="sxs-lookup"><span data-stu-id="a805a-155">INPUTS</span></span>

## <span data-ttu-id="a805a-156">輸出</span><span class="sxs-lookup"><span data-stu-id="a805a-156">OUTPUTS</span></span>

### <span data-ttu-id="a805a-157">WindowsAzure. ServiceManagement. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="a805a-157">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="a805a-158">筆記</span><span class="sxs-lookup"><span data-stu-id="a805a-158">NOTES</span></span>

## <span data-ttu-id="a805a-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="a805a-159">RELATED LINKS</span></span>

[<span data-ttu-id="a805a-160">AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="a805a-160">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="a805a-161">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a805a-161">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a805a-162">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a805a-162">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="a805a-163">新-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="a805a-163">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="a805a-164">移除-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="a805a-164">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="a805a-165">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a805a-165">Update-AzureVM</span></span>](./Update-AzureVM.md)


