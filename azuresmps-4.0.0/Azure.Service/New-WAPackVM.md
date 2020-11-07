---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968844"
---
# <span data-ttu-id="95667-101">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="95667-101">New-WAPackVM</span></span>

## <span data-ttu-id="95667-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95667-102">SYNOPSIS</span></span>
<span data-ttu-id="95667-103">建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95667-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="95667-104">句法</span><span class="sxs-lookup"><span data-stu-id="95667-104">SYNTAX</span></span>

### <span data-ttu-id="95667-105">CreateVMFromTemplate (預設) </span><span class="sxs-lookup"><span data-stu-id="95667-105">CreateVMFromTemplate (Default)</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="95667-106">CreateLinuxVMFromTemplate</span><span class="sxs-lookup"><span data-stu-id="95667-106">CreateLinuxVMFromTemplate</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="95667-107">CreateVMFromOSDisk</span><span class="sxs-lookup"><span data-stu-id="95667-107">CreateVMFromOSDisk</span></span>
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="95667-108">說明</span><span class="sxs-lookup"><span data-stu-id="95667-108">DESCRIPTION</span></span>
<span data-ttu-id="95667-109">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="95667-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="95667-110">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95667-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="95667-111">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="95667-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="95667-112">**新的-WAPackVM** Cmdlet 會建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95667-112">The **New-WAPackVM** cmdlet creates a virtual machine.</span></span>

## <span data-ttu-id="95667-113">示例</span><span class="sxs-lookup"><span data-stu-id="95667-113">EXAMPLES</span></span>

### <span data-ttu-id="95667-114">範例1：使用範本建立 Windows 作業系統的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="95667-114">Example 1: Create a virtual machine for the Windows operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

<span data-ttu-id="95667-115">第一個命令會建立一個 **PSCredential** 物件，然後將它儲存在 $Credentials 變數中。</span><span class="sxs-lookup"><span data-stu-id="95667-115">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="95667-116">此 Cmdlet 會提示您輸入帳戶和密碼。</span><span class="sxs-lookup"><span data-stu-id="95667-116">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="95667-117">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="95667-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="95667-118">第二個命令會使用 **WAPackVMTemplate** Cmdlet 取得名為 ContosoTemplate04 的虛擬機器範本，然後將它儲存在 $Template 變數中。</span><span class="sxs-lookup"><span data-stu-id="95667-118">The second command gets the virtual machine template named ContosoTemplate04 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="95667-119">最終命令會根據 $Template 變數中儲存的範本，建立一個名為 ContosoV023 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95667-119">The final command creates a virtual machine named ContosoV023, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="95667-120">此命令會指定 *windows* 參數，因此虛擬機器必須執行 windows 作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="95667-120">The command specifies the *Windows* parameter, and, therefore, the virtual machine must run a version of the Windows operating system.</span></span>

### <span data-ttu-id="95667-121">範例2：使用範本建立 Linux 作業系統的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="95667-121">Example 2: Create a virtual machine for the Linux operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

<span data-ttu-id="95667-122">第一個命令會建立一個 **PSCredential** 物件，然後將它儲存在 $Credentials 變數中。</span><span class="sxs-lookup"><span data-stu-id="95667-122">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>

<span data-ttu-id="95667-123">第二個命令會使用 **WAPackVMTemplate** Cmdlet 取得名為 ContosoTemplate19 的虛擬機器範本，然後將它儲存在 $Template 變數中。</span><span class="sxs-lookup"><span data-stu-id="95667-123">The second command gets the virtual machine template named ContosoTemplate19 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="95667-124">最終命令會根據 $Template 變數中儲存的範本，建立一個名為 ContosoV028 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95667-124">The final command creates a virtual machine named ContosoV028, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="95667-125">此命令會指定 *Linux* 參數，因此虛擬機器必須執行 Linux 作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="95667-125">The command specifies the *Linux* parameter, and, therefore, the virtual machine must run a version of the Linux operating system.</span></span>

### <span data-ttu-id="95667-126">範例3：從作業系統磁片和大小設定檔建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="95667-126">Example 3: Create a virtual machine from an operating system disk and size profile</span></span>
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

<span data-ttu-id="95667-127">第一個命令會使用 **WAPackVMOSDisk** Cmdlet 取得名為 ContosoDiskOS 的作業系統磁片，然後將它儲存在 $OSDisk 變數中。</span><span class="sxs-lookup"><span data-stu-id="95667-127">The first command gets an operating system disk named ContosoDiskOS by using the **Get-WAPackVMOSDisk** cmdlet, and then stores it in the $OSDisk variable.</span></span>

<span data-ttu-id="95667-128">第二個命令會使用 **WAPackVMSizeProfile** Cmdlet 取得名為 MediumSizeVM 的大小設定檔，然後將它儲存在 $SizeProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="95667-128">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores it in the $SizeProfile variable.</span></span>

<span data-ttu-id="95667-129">最後一個命令會從儲存在 $OSDisk 的作業系統磁片和 $SizeProfile 中儲存的大小設定檔，建立一個名為 ContosoV073 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95667-129">The final command creates a virtual machine named ContosoV073 from the operating system disk stored in $OSDisk and the size profile stored in $SizeProfile.</span></span>

## <span data-ttu-id="95667-130">參數</span><span class="sxs-lookup"><span data-stu-id="95667-130">PARAMETERS</span></span>

### <span data-ttu-id="95667-131">-AdministratorSSHKey</span><span class="sxs-lookup"><span data-stu-id="95667-131">-AdministratorSSHKey</span></span>
<span data-ttu-id="95667-132">指定管理員帳戶 (SSH) 金鑰的安全 Shell。</span><span class="sxs-lookup"><span data-stu-id="95667-132">Specifies the Secure Shell (SSH) key for the Administrator account.</span></span>

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95667-133">-Linux</span><span class="sxs-lookup"><span data-stu-id="95667-133">-Linux</span></span>
<span data-ttu-id="95667-134">表示 Cmdlet 會建立虛擬機器來執行 Linux 作業系統。</span><span class="sxs-lookup"><span data-stu-id="95667-134">Indicates that the cmdlet creates a virtual machine to run the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95667-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="95667-135">-Name</span></span>
<span data-ttu-id="95667-136">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="95667-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95667-137">-OSDisk</span><span class="sxs-lookup"><span data-stu-id="95667-137">-OSDisk</span></span>
<span data-ttu-id="95667-138">指定作業系統磁片做為 **VirtualHardDisk** 物件。</span><span class="sxs-lookup"><span data-stu-id="95667-138">Specifies an operating system disk as a **VirtualHardDisk** object.</span></span>
<span data-ttu-id="95667-139">若要取得作業系統磁片，請使用 **WAPackVMOSDisk** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95667-139">To obtain an operating system disk, use the **Get-WAPackVMOSDisk** cmdlet.</span></span>

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95667-140">-ProductKey</span><span class="sxs-lookup"><span data-stu-id="95667-140">-ProductKey</span></span>
<span data-ttu-id="95667-141">指定產品金鑰。</span><span class="sxs-lookup"><span data-stu-id="95667-141">Specifies a product key.</span></span>
<span data-ttu-id="95667-142">產品金鑰是一個用於識別產品授權的25位數數位。</span><span class="sxs-lookup"><span data-stu-id="95667-142">The product key is a 25 digit number that identifies the product license.</span></span>
<span data-ttu-id="95667-143">針對您打算在虛擬機器或主機上安裝的作業系統，使用產品金鑰。</span><span class="sxs-lookup"><span data-stu-id="95667-143">Use a product key for an operating system that you plan to install on a virtual machine or host.</span></span>

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95667-144">-設定檔</span><span class="sxs-lookup"><span data-stu-id="95667-144">-Profile</span></span>
<span data-ttu-id="95667-145">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="95667-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95667-146">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="95667-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95667-147">-範本</span><span class="sxs-lookup"><span data-stu-id="95667-147">-Template</span></span>
<span data-ttu-id="95667-148">指定範本。</span><span class="sxs-lookup"><span data-stu-id="95667-148">Specifies a template.</span></span>
<span data-ttu-id="95667-149">這個 Cmdlet 會根據您指定的範本建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95667-149">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="95667-150">若要取得範本物件，請使用 Get-WAPackVMTemplate Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95667-150">To obtain a template object, use the Get-WAPackVMTemplate cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95667-151">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="95667-151">-VMCredential</span></span>
<span data-ttu-id="95667-152">指定本機系統管理員帳戶的認證。</span><span class="sxs-lookup"><span data-stu-id="95667-152">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="95667-153">若要取得 **PSCredential** 物件，請使用 **取得認證** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95667-153">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="95667-154">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="95667-154">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95667-155">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="95667-155">-VMSizeProfile</span></span>
<span data-ttu-id="95667-156">將虛擬機器的大小設定檔指定為 **HardwareProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="95667-156">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="95667-157">若要取得大小設定檔，請使用 **WAPackVMSizeProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95667-157">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95667-158">-VNet</span><span class="sxs-lookup"><span data-stu-id="95667-158">-VNet</span></span>
<span data-ttu-id="95667-159">指定虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="95667-159">Specifies a virtual network.</span></span>
<span data-ttu-id="95667-160">此 Cmdlet 會將虛擬機器連接至您指定的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="95667-160">The cmdlet connects the virtual machine to the virtual network that you specify.</span></span>
<span data-ttu-id="95667-161">若要取得虛擬網路，請使用 **WAPackVNet** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95667-161">To obtain a virtual network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95667-162">-Windows</span><span class="sxs-lookup"><span data-stu-id="95667-162">-Windows</span></span>
<span data-ttu-id="95667-163">表示 Cmdlet 會建立虛擬機器來執行 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="95667-163">Indicates that the cmdlet creates a virtual machine to run the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95667-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95667-164">CommonParameters</span></span>
<span data-ttu-id="95667-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95667-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95667-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95667-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95667-167">輸入</span><span class="sxs-lookup"><span data-stu-id="95667-167">INPUTS</span></span>

## <span data-ttu-id="95667-168">輸出</span><span class="sxs-lookup"><span data-stu-id="95667-168">OUTPUTS</span></span>

## <span data-ttu-id="95667-169">筆記</span><span class="sxs-lookup"><span data-stu-id="95667-169">NOTES</span></span>

## <span data-ttu-id="95667-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="95667-170">RELATED LINKS</span></span>

[<span data-ttu-id="95667-171">WAPackVM</span><span class="sxs-lookup"><span data-stu-id="95667-171">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="95667-172">移除-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="95667-172">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="95667-173">重新開機-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="95667-173">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="95667-174">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="95667-174">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="95667-175">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="95667-175">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="95667-176">開始-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="95667-176">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="95667-177">停止 WAPackVM</span><span class="sxs-lookup"><span data-stu-id="95667-177">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="95667-178">暫停-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="95667-178">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="95667-179">WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="95667-179">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)

[<span data-ttu-id="95667-180">WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="95667-180">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)

[<span data-ttu-id="95667-181">WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="95667-181">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


