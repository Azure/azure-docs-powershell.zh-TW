---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: c4eef22d2bf188d56c0d7af66fb42ad3bce7b5be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904538"
---
# <span data-ttu-id="eb04a-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="eb04a-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="eb04a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb04a-102">SYNOPSIS</span></span>
<span data-ttu-id="eb04a-103">為虛擬機器新增一個秘訣。</span><span class="sxs-lookup"><span data-stu-id="eb04a-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="eb04a-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb04a-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb04a-105">描述</span><span class="sxs-lookup"><span data-stu-id="eb04a-105">DESCRIPTION</span></span>
<span data-ttu-id="eb04a-106">**Add-Az VIRTUALSecret** Cmdlet 為虛擬機器新增了一個秘訣。</span><span class="sxs-lookup"><span data-stu-id="eb04a-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="eb04a-107">此值可讓您新增憑證至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="eb04a-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="eb04a-108">機密必須儲存在金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="eb04a-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="eb04a-109">有關金鑰庫的資訊，請參閱什麼是[Azure 金鑰庫？](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="eb04a-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="eb04a-110">有關 Cmdlet 的資訊，請參閱 [Azure 金鑰庫 Cmdlet 或](/powershell/module/az.keyvault) [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb04a-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="eb04a-111">例子</span><span class="sxs-lookup"><span data-stu-id="eb04a-111">EXAMPLES</span></span>

### <span data-ttu-id="eb04a-112">範例 1：新增密碼至虛擬機器</span><span class="sxs-lookup"><span data-stu-id="eb04a-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="eb04a-113">第一個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數中。</span><span class="sxs-lookup"><span data-stu-id="eb04a-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="eb04a-114">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="eb04a-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="eb04a-115">第二個命令會使用 Get-Credential Cmdlet 建立認證物件，然後將結果儲存在$Credential變數中。</span><span class="sxs-lookup"><span data-stu-id="eb04a-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="eb04a-116">命令會提示您輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="eb04a-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="eb04a-117">如需要詳細資訊，請鍵入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="eb04a-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="eb04a-118">第三個命令使用 **Set-Az VIRTUALOperatingSystem** Cmdlet 來設定儲存在 $VirtualMachine 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="eb04a-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="eb04a-119">第四個命令會指派來源庫識別碼給$SourceVaultId變數，供日後使用。</span><span class="sxs-lookup"><span data-stu-id="eb04a-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="eb04a-120">命令會假設$SubscriptionId變數有適當的值。</span><span class="sxs-lookup"><span data-stu-id="eb04a-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="eb04a-121">第五個命令會指派值給 $CertificateStore 01 變數，供日後使用。</span><span class="sxs-lookup"><span data-stu-id="eb04a-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="eb04a-122">第六個命令會指派憑證存放區 URL。</span><span class="sxs-lookup"><span data-stu-id="eb04a-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="eb04a-123">第七個命令會為儲存在 $VirtualMachine 中的虛擬機器新增一個$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="eb04a-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="eb04a-124">SourceVaultId 參數會指定 Key Vault。</span><span class="sxs-lookup"><span data-stu-id="eb04a-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="eb04a-125">命令會指定憑證存放區的名稱，以及憑證的 URL。</span><span class="sxs-lookup"><span data-stu-id="eb04a-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="eb04a-126">您可以重複執行 **Add-AzMSSECret，** 為其他憑證新增秘訣。</span><span class="sxs-lookup"><span data-stu-id="eb04a-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="eb04a-127">參數</span><span class="sxs-lookup"><span data-stu-id="eb04a-127">PARAMETERS</span></span>

### <span data-ttu-id="eb04a-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="eb04a-128">-CertificateStore</span></span>
<span data-ttu-id="eb04a-129">指定執行 Windows 作業系統之虛擬機器上的憑證存放區名稱。</span><span class="sxs-lookup"><span data-stu-id="eb04a-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="eb04a-130">此 Cmdlet 會將憑證新增到此參數指定的儲存區。</span><span class="sxs-lookup"><span data-stu-id="eb04a-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="eb04a-131">您僅能針對執行 Windows 作業系統的虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="eb04a-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb04a-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="eb04a-132">-CertificateUrl</span></span>
<span data-ttu-id="eb04a-133">指定指向包含憑證之 Key Vault 機密的 URL。</span><span class="sxs-lookup"><span data-stu-id="eb04a-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="eb04a-134">憑證是下列 JavaScript 物件標記法 (JSON) 物件的 Base64 編碼，其編碼方式為 UTF-8：{ "data"： " \<Base64-encoded-file\> \<file-format\> password"： \<pfx-file-password\> " " } 目前，dataType 僅接受 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="eb04a-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="eb04a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb04a-135">-DefaultProfile</span></span>
<span data-ttu-id="eb04a-136">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb04a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb04a-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="eb04a-137">-SourceVaultId</span></span>
<span data-ttu-id="eb04a-138">指定金鑰庫的資源識別碼，其中包含您可以新加入虛擬機器的憑證。</span><span class="sxs-lookup"><span data-stu-id="eb04a-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="eb04a-139">此值也做為新增多個憑證的金鑰。</span><span class="sxs-lookup"><span data-stu-id="eb04a-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="eb04a-140">這表示當您從同一個金鑰庫新增多個憑證時，可以使用相同的 *SourceVaultId* 值。</span><span class="sxs-lookup"><span data-stu-id="eb04a-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb04a-141">-VM</span><span class="sxs-lookup"><span data-stu-id="eb04a-141">-VM</span></span>
<span data-ttu-id="eb04a-142">指定此 Cmdlet 修改的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="eb04a-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="eb04a-143">若要取得虛擬機器物件，請使用[Get-Az%。CMdlet。](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="eb04a-143">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="eb04a-144">您可以使用 [New-AzMSConfig](./New-AzVMConfig.md) Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="eb04a-144">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb04a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb04a-145">CommonParameters</span></span>
<span data-ttu-id="eb04a-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb04a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb04a-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb04a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb04a-148">輸入</span><span class="sxs-lookup"><span data-stu-id="eb04a-148">INPUTS</span></span>

### <span data-ttu-id="eb04a-149">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="eb04a-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="eb04a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="eb04a-150">System.String</span></span>

## <span data-ttu-id="eb04a-151">輸出</span><span class="sxs-lookup"><span data-stu-id="eb04a-151">OUTPUTS</span></span>

### <span data-ttu-id="eb04a-152">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="eb04a-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="eb04a-153">筆記</span><span class="sxs-lookup"><span data-stu-id="eb04a-153">NOTES</span></span>

## <span data-ttu-id="eb04a-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb04a-154">RELATED LINKS</span></span>

[<span data-ttu-id="eb04a-155">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="eb04a-155">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="eb04a-156">New-AzMSCONFIG</span><span class="sxs-lookup"><span data-stu-id="eb04a-156">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="eb04a-157">Set-AzEVOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="eb04a-157">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
