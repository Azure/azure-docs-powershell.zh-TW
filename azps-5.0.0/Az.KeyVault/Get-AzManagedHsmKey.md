---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
ms.openlocfilehash: 34bc2f074ee37dcf670e3e43ad647781b4d59e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136754"
---
# <span data-ttu-id="d4728-101">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d4728-101">Get-AzManagedHsmKey</span></span>

## <span data-ttu-id="d4728-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4728-102">SYNOPSIS</span></span>
<span data-ttu-id="d4728-103">取得受管理的 Hsm 金鑰。</span><span class="sxs-lookup"><span data-stu-id="d4728-103">Gets Managed Hsm keys.</span></span>

## <span data-ttu-id="d4728-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4728-104">SYNTAX</span></span>

### <span data-ttu-id="d4728-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (預設) </span><span class="sxs-lookup"><span data-stu-id="d4728-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (Default)</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4728-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="d4728-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4728-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="d4728-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4728-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="d4728-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4728-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="d4728-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4728-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="d4728-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4728-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="d4728-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4728-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="d4728-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4728-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="d4728-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4728-114">說明</span><span class="sxs-lookup"><span data-stu-id="d4728-114">DESCRIPTION</span></span>
<span data-ttu-id="d4728-115">**AzManagedHsmKey** Cmdlet 會取得 Azure 管理的 Hsm 金鑰。</span><span class="sxs-lookup"><span data-stu-id="d4728-115">The **Get-AzManagedHsmKey** cmdlet gets Azure Managed Hsm keys.</span></span>
<span data-ttu-id="d4728-116">這個 Cmdlet 會取得特定的 **KeyVault KeyBundle** 或受管理的 Hsm 或版本中所有 **KeyBundle** 物件的清單。</span><span class="sxs-lookup"><span data-stu-id="d4728-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a managed Hsm or by version.</span></span>

## <span data-ttu-id="d4728-117">示例</span><span class="sxs-lookup"><span data-stu-id="d4728-117">EXAMPLES</span></span>

### <span data-ttu-id="d4728-118">範例1：取得受管理 HSM 中的所有金鑰</span><span class="sxs-lookup"><span data-stu-id="d4728-118">Example 1: Get all the keys in a managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm
```

<span data-ttu-id="d4728-119">保存庫/HSM 名稱： testmhsm 名稱： testkey001 版本： Id： https://testmhsm.managedhsm.azure.net:443/keys/testkey001 True 到期：不早于：已更新： 10/14/2020 3:39:16 Am 更新： 10/14/2020 3:39:16 Am 恢復層級：可復原的 + Purgeable 標記：</span><span class="sxs-lookup"><span data-stu-id="d4728-119">Vault/HSM Name : testmhsm Name           : testkey001 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled        : True Expires        : Not Before     : Created        : 10/14/2020 3:39:16 AM Updated        : 10/14/2020 3:39:16 AM Recovery Level : Recoverable+Purgeable Tags           :</span></span>

<span data-ttu-id="d4728-120">保存庫/HSM 名稱： testmhsm 名稱： testkey002 版本： Id： https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled： False 到期： 10/14/2022 8:13:29 Am 不在之前： 10/14/2020 8:13:33 am 10/14/2020 8:14:01 已更新： 10/14/2020 8:14:01 Am 更新時間：可復原的 + Purgeable 標籤：名稱值嚴重性高記帳 true</span><span class="sxs-lookup"><span data-stu-id="d4728-120">Vault/HSM Name : testmhsm Name           : testkey002 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled        : False Expires        : 10/14/2022 8:13:29 AM Not Before     : 10/14/2020 8:13:33 AM Created        : 10/14/2020 8:14:01 AM Updated        : 10/14/2020 8:14:01 AM Recovery Level : Recoverable+Purgeable Tags           : Name        Value Severity    high Accounting  true</span></span>

<span data-ttu-id="d4728-121">這個命令會取得名為 testmhsm 的受管理 HSM 中的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="d4728-121">This command gets all the keys in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="d4728-122">範例2：取得目前的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="d4728-122">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\>$hsm = Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001
PS C:\>$hsm

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
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

<span data-ttu-id="d4728-123">這個命令會在受管理的 HSM （名為 testmhsm）中取得名為 testkey001 的目前金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="d4728-123">This command gets the current version of the key named testkey001 in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="d4728-124">注意： $hsm 可以取得 Hsm 名稱。VaultName</span><span class="sxs-lookup"><span data-stu-id="d4728-124">Note: Hsm Name can be obtained by $hsm.VaultName</span></span>

### <span data-ttu-id="d4728-125">範例3：取得金鑰的所有版本</span><span class="sxs-lookup"><span data-stu-id="d4728-125">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001 -IncludeVersions

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/9a9de2bcec540c3b160cd54cbae71339
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

<span data-ttu-id="d4728-126">這個命令會取得受管理的 HSM （名為 testmhsm）中名為 testkey001 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="d4728-126">This command gets all versions the key named testkey001 in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="d4728-127">範例4：取得特定的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="d4728-127">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey -Version 80fd43e31e8649873520053c91148418

Vault/HSM Name : testmhsm
Name           : testkey
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="d4728-128">這個命令會在受管理的 HSM （名為 testmhsm）中取得名為 testkey 的特定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="d4728-128">This command gets a specific version of the key named testkey in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="d4728-129">執行此命令之後，您可以流覽 $Key 物件來檢查索引鍵的各種屬性。</span><span class="sxs-lookup"><span data-stu-id="d4728-129">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="d4728-130">範例5：取得已刪除但未針對此受管理的 HSM 清除的所有索引鍵</span><span class="sxs-lookup"><span data-stu-id="d4728-130">Example 5: Get all the keys that have been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -InRemovedState

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 : Name        Value
                       Severity    high
                       Accounting  true                :
```

<span data-ttu-id="d4728-131">這個命令會在受管理的 HSM （名為 testmhsm）中，取得先前已刪除但尚未清除的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d4728-131">This command gets all the keys that have been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="d4728-132">範例6：取得已刪除但未針對此受管理的 HSM 清除的金鑰 testkey</span><span class="sxs-lookup"><span data-stu-id="d4728-132">Example 6: Gets the key testkey that has been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\>  Get-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState 

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="d4728-133">這個命令會在受管理的 HSM （名為 testmhsm）中，取得先前已刪除但尚未清除的金鑰 testkey。</span><span class="sxs-lookup"><span data-stu-id="d4728-133">This command gets the key testkey that has been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="d4728-134">這個命令會傳回中繼資料，例如刪除日期，以及此刪除金鑰的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="d4728-134">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="d4728-135">範例7：使用篩選取得受管理 HSM 中的所有金鑰</span><span class="sxs-lookup"><span data-stu-id="d4728-135">Example 7: Get all the keys in a managed HSM using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName "test*"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="d4728-136">這個命令會取得名為 testmhsm 的受管理 HSM 中以「test」開頭的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d4728-136">This command gets all the keys in the managed HSM named testmhsm that start with "test".</span></span>

### <span data-ttu-id="d4728-137">範例8：下載公開金鑰做為 pem 檔案</span><span class="sxs-lookup"><span data-stu-id="d4728-137">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> Get-AzManagedHsmKey -HsmName bezmhsm -Name testkey -OutFile  "C:\public.pem"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="d4728-138">您可以透過指定參數來下載 RSA 金鑰的公開金鑰 `-OutFile` 。</span><span class="sxs-lookup"><span data-stu-id="d4728-138">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>

## <span data-ttu-id="d4728-139">參數</span><span class="sxs-lookup"><span data-stu-id="d4728-139">PARAMETERS</span></span>

### <span data-ttu-id="d4728-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4728-140">-DefaultProfile</span></span>
<span data-ttu-id="d4728-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4728-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4728-142">-HsmName</span><span class="sxs-lookup"><span data-stu-id="d4728-142">-HsmName</span></span>
<span data-ttu-id="d4728-143">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="d4728-143">HSM name.</span></span> <span data-ttu-id="d4728-144">Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d4728-144">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4728-145">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="d4728-145">-IncludeVersions</span></span>
<span data-ttu-id="d4728-146">指定是否要在輸出中包含金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="d4728-146">Specifies whether to include the versions of the key in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4728-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4728-147">-InputObject</span></span>
<span data-ttu-id="d4728-148">HSM 物件。</span><span class="sxs-lookup"><span data-stu-id="d4728-148">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4728-149">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d4728-149">-InRemovedState</span></span>
<span data-ttu-id="d4728-150">指定是否要在輸出中顯示先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="d4728-150">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4728-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4728-151">-Name</span></span>
<span data-ttu-id="d4728-152">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="d4728-152">Key name.</span></span>
<span data-ttu-id="d4728-153">Cmdlet 會從 managed HSM 名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d4728-153">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4728-154">-OutFile</span><span class="sxs-lookup"><span data-stu-id="d4728-154">-OutFile</span></span>
<span data-ttu-id="d4728-155">指定此 Cmdlet 儲存金鑰的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="d4728-155">Specifies the output file for which this cmdlet saves the key.</span></span>
<span data-ttu-id="d4728-156">公開金鑰預設會以 PEM 格式儲存。</span><span class="sxs-lookup"><span data-stu-id="d4728-156">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="d4728-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4728-157">-ResourceId</span></span>
<span data-ttu-id="d4728-158">HSM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4728-158">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByResourceIdGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4728-159">-版本</span><span class="sxs-lookup"><span data-stu-id="d4728-159">-Version</span></span>
<span data-ttu-id="d4728-160">金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="d4728-160">Key version.</span></span>
<span data-ttu-id="d4728-161">Cmdlet 會從 managed HSM 名稱、目前已選取的環境、金鑰名稱和金鑰版本構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d4728-161">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4728-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4728-162">CommonParameters</span></span>
<span data-ttu-id="d4728-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4728-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4728-164">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d4728-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4728-165">輸入</span><span class="sxs-lookup"><span data-stu-id="d4728-165">INPUTS</span></span>

### <span data-ttu-id="d4728-166">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="d4728-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="d4728-167">System.object</span><span class="sxs-lookup"><span data-stu-id="d4728-167">System.String</span></span>

## <span data-ttu-id="d4728-168">輸出</span><span class="sxs-lookup"><span data-stu-id="d4728-168">OUTPUTS</span></span>

### <span data-ttu-id="d4728-169">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="d4728-169">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="d4728-170">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="d4728-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="d4728-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d4728-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="d4728-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d4728-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="d4728-173">筆記</span><span class="sxs-lookup"><span data-stu-id="d4728-173">NOTES</span></span>

## <span data-ttu-id="d4728-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4728-174">RELATED LINKS</span></span>

[<span data-ttu-id="d4728-175">附加 AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d4728-175">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="d4728-176">備份-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d4728-176">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="d4728-177">移除-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d4728-177">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="d4728-178">復原-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="d4728-178">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="d4728-179">更新-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d4728-179">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="d4728-180">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d4728-180">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)