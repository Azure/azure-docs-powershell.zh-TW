---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
ms.openlocfilehash: 89238992b99d86cdd56337a3002167be9c0d78d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141679"
---
# <span data-ttu-id="ba926-101">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ba926-101">Add-AzManagedHsmKey</span></span>

## <span data-ttu-id="ba926-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba926-102">SYNOPSIS</span></span>
<span data-ttu-id="ba926-103">在 managed HSM 中建立金鑰，或將金鑰匯入受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="ba926-103">Creates a key in a managed HSM or imports a key into a managed HSM.</span></span>

## <span data-ttu-id="ba926-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba926-104">SYNTAX</span></span>

### <span data-ttu-id="ba926-105">InteractiveCreate (預設) </span><span class="sxs-lookup"><span data-stu-id="ba926-105">InteractiveCreate (Default)</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba926-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="ba926-106">InteractiveImport</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba926-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="ba926-107">InputObjectCreate</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyType <String> [-CurveName <String>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-Size <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba926-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="ba926-108">InputObjectImport</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba926-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="ba926-109">ResourceIdCreate</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba926-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="ba926-110">ResourceIdImport</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba926-111">說明</span><span class="sxs-lookup"><span data-stu-id="ba926-111">DESCRIPTION</span></span>
<span data-ttu-id="ba926-112">AzManagedHsmKey Cmdlet 會在 Azure Managed Hsm 的受管理 HSM 中建立金鑰，或 **將** 金鑰匯入受管理的 hsm。</span><span class="sxs-lookup"><span data-stu-id="ba926-112">The **Add-AzManagedHsmKey** cmdlet creates a key in a managed HSM in Azure Managed Hsm or imports a key into a managed HSM.</span></span>
<span data-ttu-id="ba926-113">使用這個 Cmdlet，使用下列任何一種方法來新增金鑰：</span><span class="sxs-lookup"><span data-stu-id="ba926-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="ba926-114">使用預設的索引鍵屬性建立索引鍵</span><span class="sxs-lookup"><span data-stu-id="ba926-114">Create a key with default key attributes</span></span>
- <span data-ttu-id="ba926-115">使用指定的鍵屬性建立金鑰</span><span class="sxs-lookup"><span data-stu-id="ba926-115">Create a key with given key attributes</span></span>
- <span data-ttu-id="ba926-116">從您電腦上的 .pfx 檔案匯入金鑰。</span><span class="sxs-lookup"><span data-stu-id="ba926-116">Import a key from a .pfx file on your computer.</span></span>
<span data-ttu-id="ba926-117">針對這些作業中的任何一個，您可以提供重要屬性或接受預設設定。</span><span class="sxs-lookup"><span data-stu-id="ba926-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="ba926-118">如果您在受管理的 HSM 中建立或匯入與現有金鑰同名的金鑰，則會使用您為新金鑰指定的值來更新原始金鑰。</span><span class="sxs-lookup"><span data-stu-id="ba926-118">If you create or import a key that has the same name as an existing key in your managed HSM, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="ba926-119">您可以使用該版本金鑰的版本特定 URI 來存取先前的值。</span><span class="sxs-lookup"><span data-stu-id="ba926-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="ba926-120">若要瞭解主要版本與 URI 結構，請參閱關於受管理的 HSM REST API 檔中的 [金鑰與密碼](http://go.microsoft.com/fwlink/?linkid=518560) 。</span><span class="sxs-lookup"><span data-stu-id="ba926-120">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Managed HSM REST API documentation.</span></span>

## <span data-ttu-id="ba926-121">示例</span><span class="sxs-lookup"><span data-stu-id="ba926-121">EXAMPLES</span></span>

### <span data-ttu-id="ba926-122">範例1：建立 RSA-HSM 金鑰</span><span class="sxs-lookup"><span data-stu-id="ba926-122">Example 1: Create a RSA-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType RSA

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 7:55:43 AM
Updated        : 10/14/2020 7:55:43 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="ba926-123">這個命令會在受管理的 HSM testkey （名為 testmhsm）中建立名為 testkey 的 RSA HSM 金鑰。</span><span class="sxs-lookup"><span data-stu-id="ba926-123">This command creates a RSA-HSM key named testkey in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="ba926-124">範例2：建立 EC-HSM 金鑰</span><span class="sxs-lookup"><span data-stu-id="ba926-124">Example 2: Create a EC-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType EC -CurveName P-256

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="ba926-125">這個命令會建立一個名為 testkey 的 EC HSM 金鑰，在名為 testmhsm 的 managed HSM testkey 中使用 P-256 曲線。</span><span class="sxs-lookup"><span data-stu-id="ba926-125">This command creates a EC-HSM key named testkey using P-256 curve in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="ba926-126">範例3：建立含非預設值的10月 HSM 金鑰</span><span class="sxs-lookup"><span data-stu-id="ba926-126">Example 3: Create a oct-HSM key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType oct -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="ba926-127">第一個命令會儲存在 $KeyOperations 變數中解密和驗證的值。</span><span class="sxs-lookup"><span data-stu-id="ba926-127">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="ba926-128">第二個命令會建立一個 **DateTime** 物件（在 UTC 中定義），方法是使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba926-128">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="ba926-129">該物件指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="ba926-129">That object specifies a time two years in the future.</span></span> <span data-ttu-id="ba926-130">該命令會將該日期儲存在 $Expires 變數中。</span><span class="sxs-lookup"><span data-stu-id="ba926-130">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="ba926-131">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="ba926-131">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="ba926-132">第三個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="ba926-132">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="ba926-133">該物件會指定目前的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="ba926-133">That object specifies current UTC time.</span></span> <span data-ttu-id="ba926-134">該命令會將該日期儲存在 $NotBefore 變數中。</span><span class="sxs-lookup"><span data-stu-id="ba926-134">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="ba926-135">最後一個命令會建立一個名為 testkey 的索引鍵，該金鑰是一個10月的 HSM 金鑰。</span><span class="sxs-lookup"><span data-stu-id="ba926-135">The final command creates a key named testkey that is an oct-HSM key.</span></span> <span data-ttu-id="ba926-136">此命令會指定儲存 $KeyOperations 所允許的按鍵作業值。</span><span class="sxs-lookup"><span data-stu-id="ba926-136">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="ba926-137">此命令會指定在前一個命令中建立的 *Expires* 及 *NotBefore* 參數的時間，以及高嚴重性及嚴重度的標記。</span><span class="sxs-lookup"><span data-stu-id="ba926-137">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="ba926-138">新的索引鍵是停用的。</span><span class="sxs-lookup"><span data-stu-id="ba926-138">The new key is disabled.</span></span> <span data-ttu-id="ba926-139">您可以使用 **AzManagedHsmKey** Cmdlet 來啟用它。</span><span class="sxs-lookup"><span data-stu-id="ba926-139">You can enable it by using the **Update-AzManagedHsmKey** cmdlet.</span></span>

## <span data-ttu-id="ba926-140">參數</span><span class="sxs-lookup"><span data-stu-id="ba926-140">PARAMETERS</span></span>

### <span data-ttu-id="ba926-141">-CurveName</span><span class="sxs-lookup"><span data-stu-id="ba926-141">-CurveName</span></span>
<span data-ttu-id="ba926-142">指定橢圓曲線密碼加密的曲線名稱，此值在 KeyType 為 EC 時有效。</span><span class="sxs-lookup"><span data-stu-id="ba926-142">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba926-143">-DefaultProfile</span></span>
<span data-ttu-id="ba926-144">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba926-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba926-145">-停用</span><span class="sxs-lookup"><span data-stu-id="ba926-145">-Disable</span></span>
<span data-ttu-id="ba926-146">表示您要新增的金鑰已設定為 [已停用] 的初始狀態。</span><span class="sxs-lookup"><span data-stu-id="ba926-146">Indicates that the key you are adding is set to an initial state of disabled.</span></span>
<span data-ttu-id="ba926-147">任何使用金鑰的嘗試都將失敗。</span><span class="sxs-lookup"><span data-stu-id="ba926-147">Any attempt to use the key will fail.</span></span>
<span data-ttu-id="ba926-148">如果您正在預載入您想要稍後啟用的金鑰，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="ba926-148">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="ba926-149">-到期</span><span class="sxs-lookup"><span data-stu-id="ba926-149">-Expires</span></span>
<span data-ttu-id="ba926-150">指定 UTC 中金鑰的到期時間。</span><span class="sxs-lookup"><span data-stu-id="ba926-150">Specifies the expiration time of the key in UTC.</span></span>
<span data-ttu-id="ba926-151">如果未指定，金鑰就不會過期。</span><span class="sxs-lookup"><span data-stu-id="ba926-151">If not specified, key will not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-152">-HsmName</span><span class="sxs-lookup"><span data-stu-id="ba926-152">-HsmName</span></span>
<span data-ttu-id="ba926-153">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="ba926-153">HSM name.</span></span> <span data-ttu-id="ba926-154">Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ba926-154">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-155">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba926-155">-InputObject</span></span>
<span data-ttu-id="ba926-156">HSM 物件。</span><span class="sxs-lookup"><span data-stu-id="ba926-156">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-157">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="ba926-157">-KeyFilePassword</span></span>
<span data-ttu-id="ba926-158">包含要匯入之金鑰資料之本機檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="ba926-158">Password of the local file containing the key material to be imported.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-159">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="ba926-159">-KeyFilePath</span></span>
<span data-ttu-id="ba926-160">包含要匯入之金鑰資料之本機檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="ba926-160">Path to the local file containing the key material to be imported.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-161">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="ba926-161">-KeyOps</span></span>
<span data-ttu-id="ba926-162">可使用金鑰執行的作業。</span><span class="sxs-lookup"><span data-stu-id="ba926-162">The operations that can be performed with the key.</span></span>
<span data-ttu-id="ba926-163">如果不存在，則可以執行所有作業。</span><span class="sxs-lookup"><span data-stu-id="ba926-163">If not present, all operations can be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-164">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ba926-164">-KeyType</span></span>
<span data-ttu-id="ba926-165">指定此金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="ba926-165">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-166">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba926-166">-Name</span></span>
<span data-ttu-id="ba926-167">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="ba926-167">Key name.</span></span>
<span data-ttu-id="ba926-168">Cmdlet 會從 managed HSM 名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ba926-168">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-169">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="ba926-169">-NotBefore</span></span>
<span data-ttu-id="ba926-170">在哪個 UTC 時間之前無法使用該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ba926-170">The UTC time before which the key can't be used.</span></span>
<span data-ttu-id="ba926-171">如果未指定，就沒有限制。</span><span class="sxs-lookup"><span data-stu-id="ba926-171">If not specified, there is no limitation.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-172">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba926-172">-ResourceId</span></span>
<span data-ttu-id="ba926-173">HSM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba926-173">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-174">-大小</span><span class="sxs-lookup"><span data-stu-id="ba926-174">-Size</span></span>
<span data-ttu-id="ba926-175">RSA 金鑰大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="ba926-175">RSA key size, in bits.</span></span>
<span data-ttu-id="ba926-176">如果未指定，服務將會提供安全的預設值。</span><span class="sxs-lookup"><span data-stu-id="ba926-176">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-177">-Tag</span><span class="sxs-lookup"><span data-stu-id="ba926-177">-Tag</span></span>
<span data-ttu-id="ba926-178">代表主要標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="ba926-178">A hashtable representing key tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-179">-確認</span><span class="sxs-lookup"><span data-stu-id="ba926-179">-Confirm</span></span>
<span data-ttu-id="ba926-180">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba926-180">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba926-181">-WhatIf</span></span>
<span data-ttu-id="ba926-182">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba926-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba926-183">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba926-183">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba926-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba926-184">CommonParameters</span></span>
<span data-ttu-id="ba926-185">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba926-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba926-186">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ba926-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba926-187">輸入</span><span class="sxs-lookup"><span data-stu-id="ba926-187">INPUTS</span></span>

### <span data-ttu-id="ba926-188">PSManagedHsm 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="ba926-188">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="ba926-189">System.object</span><span class="sxs-lookup"><span data-stu-id="ba926-189">System.String</span></span>

## <span data-ttu-id="ba926-190">輸出</span><span class="sxs-lookup"><span data-stu-id="ba926-190">OUTPUTS</span></span>

### <span data-ttu-id="ba926-191">PSManagedHsm 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="ba926-191">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="ba926-192">筆記</span><span class="sxs-lookup"><span data-stu-id="ba926-192">NOTES</span></span>

## <span data-ttu-id="ba926-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba926-193">RELATED LINKS</span></span>

[<span data-ttu-id="ba926-194">備份-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ba926-194">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="ba926-195">AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ba926-195">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="ba926-196">移除-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ba926-196">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="ba926-197">復原-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="ba926-197">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="ba926-198">更新-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ba926-198">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="ba926-199">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ba926-199">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)
