---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967428"
---
# <span data-ttu-id="6d265-101">New-AzureSSHKey</span><span class="sxs-lookup"><span data-stu-id="6d265-101">New-AzureSSHKey</span></span>

## <span data-ttu-id="6d265-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d265-102">SYNOPSIS</span></span>
<span data-ttu-id="6d265-103">建立 SSH 金鑰組象，以在新的 Linux 專用 Azure 虛擬機器中插入現有的憑證。</span><span class="sxs-lookup"><span data-stu-id="6d265-103">Creates a SSH Key object to insert an existing certificate into a new Linux-based Azure virtual machines.</span></span>

## <span data-ttu-id="6d265-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d265-104">SYNTAX</span></span>

### <span data-ttu-id="6d265-105">金鑰</span><span class="sxs-lookup"><span data-stu-id="6d265-105">keypair</span></span>
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6d265-106">publickey</span><span class="sxs-lookup"><span data-stu-id="6d265-106">publickey</span></span>
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6d265-107">說明</span><span class="sxs-lookup"><span data-stu-id="6d265-107">DESCRIPTION</span></span>
<span data-ttu-id="6d265-108">**新的-AzureSSHKey** Cmdlet 會為已新增至 Azure 的憑證建立 SSH 金鑰組象。</span><span class="sxs-lookup"><span data-stu-id="6d265-108">The **New-AzureSSHKey** cmdlet creates an SSH Key object for a certificate that has already been added to Azure.</span></span>
<span data-ttu-id="6d265-109">當您使用 **新** 的新虛擬機器建立 configuration 物件時，或是使用 **新的 AzureQuickVM** 建立新的虛擬機器時，可以使用此 SSH 金鑰組象來供 **新 AzureProvisioningConfig** 使用。</span><span class="sxs-lookup"><span data-stu-id="6d265-109">This SSH Key object can then be used by **New-AzureProvisioningConfig** when creating the configuration object for a new virtual machine using **New-AzureVM** , or when creating a new virtual machine with **New-AzureQuickVM**.</span></span>
<span data-ttu-id="6d265-110">當包含為虛擬機器建立腳本的一部分時，會將指定的 SSH 公開金鑰或金鑰組新增至新的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6d265-110">When included as part of a virtual machine creation script, this adds the specified SSH Public Key or Key Pair to the new virtual machine.</span></span>

## <span data-ttu-id="6d265-111">示例</span><span class="sxs-lookup"><span data-stu-id="6d265-111">EXAMPLES</span></span>

### <span data-ttu-id="6d265-112">範例1：建立憑證設定物件</span><span class="sxs-lookup"><span data-stu-id="6d265-112">Example 1: Create a certificate setting object</span></span>
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

<span data-ttu-id="6d265-113">這個命令會建立現有憑證的憑證設定物件，然後將物件儲存在變數中供日後使用。</span><span class="sxs-lookup"><span data-stu-id="6d265-113">This command creates a certificate setting object for an existing certificate and then stores the object in a variable for later use.</span></span>

### <span data-ttu-id="6d265-114">範例2：新增憑證至服務</span><span class="sxs-lookup"><span data-stu-id="6d265-114">Example 2: Add a certificate to a service</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

<span data-ttu-id="6d265-115">這個命令會將憑證新增到 Azure 服務，然後建立新的使用憑證的 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6d265-115">This command adds a certificate to an Azure service, and then creates a new Linux virtual machine that uses the certificate.</span></span>

## <span data-ttu-id="6d265-116">參數</span><span class="sxs-lookup"><span data-stu-id="6d265-116">PARAMETERS</span></span>

### <span data-ttu-id="6d265-117">-指紋</span><span class="sxs-lookup"><span data-stu-id="6d265-117">-Fingerprint</span></span>
<span data-ttu-id="6d265-118">指定憑證的指紋。</span><span class="sxs-lookup"><span data-stu-id="6d265-118">Specifies the fingerprint of the certificate.</span></span>

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

### <span data-ttu-id="6d265-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6d265-119">-InformationAction</span></span>
<span data-ttu-id="6d265-120">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="6d265-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6d265-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6d265-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d265-122">持續</span><span class="sxs-lookup"><span data-stu-id="6d265-122">Continue</span></span>
- <span data-ttu-id="6d265-123">理會</span><span class="sxs-lookup"><span data-stu-id="6d265-123">Ignore</span></span>
- <span data-ttu-id="6d265-124">看</span><span class="sxs-lookup"><span data-stu-id="6d265-124">Inquire</span></span>
- <span data-ttu-id="6d265-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6d265-125">SilentlyContinue</span></span>
- <span data-ttu-id="6d265-126">停止</span><span class="sxs-lookup"><span data-stu-id="6d265-126">Stop</span></span>
- <span data-ttu-id="6d265-127">封存</span><span class="sxs-lookup"><span data-stu-id="6d265-127">Suspend</span></span>

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

### <span data-ttu-id="6d265-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6d265-128">-InformationVariable</span></span>
<span data-ttu-id="6d265-129">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="6d265-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6d265-130">-金鑰組</span><span class="sxs-lookup"><span data-stu-id="6d265-130">-KeyPair</span></span>
<span data-ttu-id="6d265-131">指定此 Cmdlet 會建立一個物件，以將 SSH 金鑰組插入新的虛擬機器配置中。</span><span class="sxs-lookup"><span data-stu-id="6d265-131">Specifies that this cmdlet creates an object for inserting an SSH Key Pair into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d265-132">-Path</span><span class="sxs-lookup"><span data-stu-id="6d265-132">-Path</span></span>
<span data-ttu-id="6d265-133">指定儲存 SSH 公開金鑰或金鑰組的路徑。</span><span class="sxs-lookup"><span data-stu-id="6d265-133">Specifies the path to store the SSH Public Key or Key Pair.</span></span>

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

### <span data-ttu-id="6d265-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="6d265-134">-PublicKey</span></span>
<span data-ttu-id="6d265-135">指定此 Cmdlet 會建立一個物件，以將 SSH 公開金鑰插入新的虛擬機器配置中。</span><span class="sxs-lookup"><span data-stu-id="6d265-135">Specifies that this cmdlet creates an object for inserting an SSH Public Key into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d265-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d265-136">CommonParameters</span></span>
<span data-ttu-id="6d265-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d265-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d265-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6d265-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d265-139">輸入</span><span class="sxs-lookup"><span data-stu-id="6d265-139">INPUTS</span></span>

## <span data-ttu-id="6d265-140">輸出</span><span class="sxs-lookup"><span data-stu-id="6d265-140">OUTPUTS</span></span>

## <span data-ttu-id="6d265-141">筆記</span><span class="sxs-lookup"><span data-stu-id="6d265-141">NOTES</span></span>

## <span data-ttu-id="6d265-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d265-142">RELATED LINKS</span></span>

[<span data-ttu-id="6d265-143">附加 AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="6d265-143">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="6d265-144">新-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="6d265-144">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="6d265-145">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="6d265-145">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="6d265-146">新-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="6d265-146">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


