---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
ms.openlocfilehash: 0b1cc516f4ca3e434c0cc5e6dfe47b199ad509a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799838"
---
# <span data-ttu-id="3cd27-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="3cd27-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="3cd27-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3cd27-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd27-103">針對特定的主要電子倉庫管理的 Azure 儲存空間帳戶，使用金鑰保存庫 (SAS) 定義來設定共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="3cd27-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cd27-104">句法</span><span class="sxs-lookup"><span data-stu-id="3cd27-104">SYNTAX</span></span>

### <span data-ttu-id="3cd27-105">RawSas (預設) </span><span class="sxs-lookup"><span data-stu-id="3cd27-105">RawSas (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Parameter] <Hashtable> [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd27-106">AdhocAccountSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-106">AdhocAccountSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition -Service <String[]> -ResourceType <String[]>
 [-ApiVersion <String>] [-VaultName] <String> [-AccountName] <String> [-Name] <String> [-Disable]
 [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>] [-IPAddressOrRange <String>]
 -ValidityPeriod <TimeSpan> -Permission <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd27-107">AdhocServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-107">AdhocServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Blob <String>
 -Container <String> [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd27-108">AdhocServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-108">AdhocServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Container <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cd27-109">AdhocServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-109">AdhocServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd27-110">AdhocServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-110">AdhocServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd27-111">AdhocServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-111">AdhocServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Queue <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd27-112">AdhocServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-112">AdhocServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Table <String>
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd27-113">StoredPolicyServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-113">StoredPolicyServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Blob <String> -Container <String> -Policy <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cd27-114">StoredPolicyServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-114">StoredPolicyServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Container <String> -Policy <String> [-SharedAccessHeader <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd27-115">StoredPolicyServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-115">StoredPolicyServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String> -Path <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd27-116">StoredPolicyServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-116">StoredPolicyServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd27-117">StoredPolicyServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-117">StoredPolicyServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Queue <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd27-118">StoredPolicyServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="3cd27-118">StoredPolicyServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Table <String> [-StartPartitionKey <String>]
 [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cd27-119">說明</span><span class="sxs-lookup"><span data-stu-id="3cd27-119">DESCRIPTION</span></span>
<span data-ttu-id="3cd27-120">使用指定的主要電子倉庫管理的 Azure 儲存空間帳戶，設定共用存取簽章 (SAS) 定義。</span><span class="sxs-lookup"><span data-stu-id="3cd27-120">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="3cd27-121">這也會設定一個機密，您可以用來針對每個 SAS 定義取得 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="3cd27-121">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="3cd27-122">SAS 權杖是使用這些參數以及主要電子倉庫管理的 Azure 儲存空間帳戶的活動金鑰產生。</span><span class="sxs-lookup"><span data-stu-id="3cd27-122">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="3cd27-123">示例</span><span class="sxs-lookup"><span data-stu-id="3cd27-123">EXAMPLES</span></span>

### <span data-ttu-id="3cd27-124">範例1：設定 ad hoc 服務 Blob sas 定義</span><span class="sxs-lookup"><span data-stu-id="3cd27-124">Example 1 : Set an ad hoc service Blob sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Blob 'blob1' -Container 'container1' -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add -SharedAccessHeader CacheControl,ContentDisposition -Protocol HttpsOnly -IPAddressOrRange '168.1.5.60-168.1.5.70'
```

<span data-ttu-id="3cd27-125">使用保存庫 [vault1] 中的主要保存庫管理的儲存空間帳戶 ' 帳戶 1 ' 設定 ad hoc 服務 blob sas 定義 ' sas1」。</span><span class="sxs-lookup"><span data-stu-id="3cd27-125">Sets an ad hoc service blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="3cd27-126">範例2：設定 ad hoc 帳戶 sas 定義</span><span class="sxs-lookup"><span data-stu-id="3cd27-126">Example 2 : Set an ad hoc account sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob,File -ResourceType Container,Service -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -Protocol HttpsOrHttp -IPAddressOrRange '168.1.5.60' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add
```

<span data-ttu-id="3cd27-127">使用保存庫 [vault1 "中的主要保存庫管理的儲存空間帳戶 ' 帳戶 1 ' 設定 ad hoc blob sas 定義 ' sas1」。</span><span class="sxs-lookup"><span data-stu-id="3cd27-127">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="3cd27-128">範例3：使用 hashtable 設定 sas 定義</span><span class="sxs-lookup"><span data-stu-id="3cd27-128">Example 3 : Set a sas definition using a hashtable</span></span>
```
PS C:\> $parameters = @{"sasType"="blob";"signedVersion"="2016-05-31";"signedProtocols"="https";"signedIp"="168.1.5.60-168.1.5.70";"validityPeriod"="P30D";"signedPermissions"="ra";"blobName"="blob1";"containerName"="container1";"rscd"="";"rscc"=""}
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -VaultName vault1 -AccountName account1 -Name sas1 -Parameter $parameters
```

<span data-ttu-id="3cd27-129">使用 hashtable 來設定保存庫 [vault1] 中的主要 blob sas 定義 ' sas1 ' （含金鑰儲存管理儲存帳戶 ' 帳戶1」）。</span><span class="sxs-lookup"><span data-stu-id="3cd27-129">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1' using a hashtable.</span></span>

## <span data-ttu-id="3cd27-130">參數</span><span class="sxs-lookup"><span data-stu-id="3cd27-130">PARAMETERS</span></span>

### <span data-ttu-id="3cd27-131">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3cd27-131">-AccountName</span></span>
<span data-ttu-id="3cd27-132">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3cd27-132">Key Vault managed storage account name.</span></span> <span data-ttu-id="3cd27-133">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="3cd27-133">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3cd27-134">-ApiVersion</span></span>
<span data-ttu-id="3cd27-135">指定要用來執行使用帳戶 SAS URI 發出之要求的儲存服務版本。</span><span class="sxs-lookup"><span data-stu-id="3cd27-135">Specifies the storage service version to use to execute the request made using the account SAS URI.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-136">-Blob</span><span class="sxs-lookup"><span data-stu-id="3cd27-136">-Blob</span></span>
<span data-ttu-id="3cd27-137">Blob 名稱</span><span class="sxs-lookup"><span data-stu-id="3cd27-137">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, StoredPolicyServiceBlobSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-138">-容器</span><span class="sxs-lookup"><span data-stu-id="3cd27-138">-Container</span></span>
<span data-ttu-id="3cd27-139">容器名稱</span><span class="sxs-lookup"><span data-stu-id="3cd27-139">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd27-140">-DefaultProfile</span></span>
<span data-ttu-id="3cd27-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3cd27-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cd27-142">-停用</span><span class="sxs-lookup"><span data-stu-id="3cd27-142">-Disable</span></span>
<span data-ttu-id="3cd27-143">停用 sas 定義來產生 sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="3cd27-143">Disables the use of sas definition for generation of sas token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-144">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="3cd27-144">-EndPartitionKey</span></span>
<span data-ttu-id="3cd27-145">結束分區鍵</span><span class="sxs-lookup"><span data-stu-id="3cd27-145">End Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-146">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="3cd27-146">-EndRowKey</span></span>
<span data-ttu-id="3cd27-147">[結束列] 索引鍵</span><span class="sxs-lookup"><span data-stu-id="3cd27-147">End Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-148">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3cd27-148">-IPAddressOrRange</span></span>
<span data-ttu-id="3cd27-149">IP 或 IP 範圍 ACL (存取控制) 清單，以供 Azure 存儲接受的要求。</span><span class="sxs-lookup"><span data-stu-id="3cd27-149">IP, or IP range ACL (access control list) of the request that would be accepted by Azure Storage.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="3cd27-150">-Name</span></span>
<span data-ttu-id="3cd27-151">儲存區 sas 定義名稱。</span><span class="sxs-lookup"><span data-stu-id="3cd27-151">Storage sas definition name.</span></span> <span data-ttu-id="3cd27-152">Cmdlet 會從保存庫名稱、目前所選的環境、儲存空間帳戶名稱和 sas 定義名稱來構造儲存 sas 定義的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="3cd27-152">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-153">-參數</span><span class="sxs-lookup"><span data-stu-id="3cd27-153">-Parameter</span></span>
<span data-ttu-id="3cd27-154">將用來建立 sas 權杖的 Sas 定義參數。</span><span class="sxs-lookup"><span data-stu-id="3cd27-154">Sas definition parameters that will be used to create the sas token.</span></span>

```yaml
Type: Hashtable
Parameter Sets: RawSas
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-155">-Path</span><span class="sxs-lookup"><span data-stu-id="3cd27-155">-Path</span></span>
<span data-ttu-id="3cd27-156">要產生 sas 標記的雲端檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="3cd27-156">Path to the cloud file to generate sas token against.</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, StoredPolicyServiceFileSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-157">-許可權</span><span class="sxs-lookup"><span data-stu-id="3cd27-157">-Permission</span></span>
<span data-ttu-id="3cd27-158">拒絕.</span><span class="sxs-lookup"><span data-stu-id="3cd27-158">Permission.</span></span> <span data-ttu-id="3cd27-159">值包含 "Query"、"Add"、"Update"、"Process"</span><span class="sxs-lookup"><span data-stu-id="3cd27-159">Values include 'Query','Add','Update','Process'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 
Accepted values: Add, Create, Delete, List, Process, Read, Query, Update, Write

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-160">-原則</span><span class="sxs-lookup"><span data-stu-id="3cd27-160">-Policy</span></span>
<span data-ttu-id="3cd27-161">原則識別碼</span><span class="sxs-lookup"><span data-stu-id="3cd27-161">Policy Identifier</span></span>

```yaml
Type: String
Parameter Sets: StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-162">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="3cd27-162">-Protocol</span></span>
<span data-ttu-id="3cd27-163">您可以在含 SAS 權杖的要求中使用通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3cd27-163">Protocol can be used in the request with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-164">-佇列</span><span class="sxs-lookup"><span data-stu-id="3cd27-164">-Queue</span></span>
<span data-ttu-id="3cd27-165">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="3cd27-165">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceQueueSas, StoredPolicyServiceQueueSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-166">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3cd27-166">-ResourceType</span></span>
<span data-ttu-id="3cd27-167">此 SAS 權杖適用的資源類型。</span><span class="sxs-lookup"><span data-stu-id="3cd27-167">Resource types that this SAS token applies to.</span></span> <span data-ttu-id="3cd27-168">值包括 "Service"、"Container"、"Object"</span><span class="sxs-lookup"><span data-stu-id="3cd27-168">Values include 'Service','Container','Object'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-169">-服務</span><span class="sxs-lookup"><span data-stu-id="3cd27-169">-Service</span></span>
<span data-ttu-id="3cd27-170">此 SAS 權杖適用的服務類型。</span><span class="sxs-lookup"><span data-stu-id="3cd27-170">Service types that this SAS token applies to.</span></span> <span data-ttu-id="3cd27-171">值包含 "Blob"，"File"，"Queue"，"Table"</span><span class="sxs-lookup"><span data-stu-id="3cd27-171">Values include 'Blob','File','Queue','Table'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-172">-共用</span><span class="sxs-lookup"><span data-stu-id="3cd27-172">-Share</span></span>
<span data-ttu-id="3cd27-173">共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="3cd27-173">Share Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-174">-SharedAccessHeader</span><span class="sxs-lookup"><span data-stu-id="3cd27-174">-SharedAccessHeader</span></span>
<span data-ttu-id="3cd27-175">指定要覆寫回應標頭的查詢參數。</span><span class="sxs-lookup"><span data-stu-id="3cd27-175">Specifies the query parameters to override response headers.</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 
Accepted values: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-176">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="3cd27-176">-StartPartitionKey</span></span>
<span data-ttu-id="3cd27-177">啟動磁碟分割鍵</span><span class="sxs-lookup"><span data-stu-id="3cd27-177">Start Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-178">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="3cd27-178">-StartRowKey</span></span>
<span data-ttu-id="3cd27-179">起始列鍵</span><span class="sxs-lookup"><span data-stu-id="3cd27-179">Start Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-180">-資料表</span><span class="sxs-lookup"><span data-stu-id="3cd27-180">-Table</span></span>
<span data-ttu-id="3cd27-181">資料表名稱</span><span class="sxs-lookup"><span data-stu-id="3cd27-181">Table Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="3cd27-182">-Tag</span></span>
<span data-ttu-id="3cd27-183">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="3cd27-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3cd27-184">例如：</span><span class="sxs-lookup"><span data-stu-id="3cd27-184">For example:</span></span>

<span data-ttu-id="3cd27-185">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3cd27-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-186">-TargetStorageVersion</span><span class="sxs-lookup"><span data-stu-id="3cd27-186">-TargetStorageVersion</span></span>
<span data-ttu-id="3cd27-187">指定已簽署的儲存服務版本，以用來驗證使用 SAS 權杖所進行的要求。</span><span class="sxs-lookup"><span data-stu-id="3cd27-187">Specifies the signed storage service version to use to authenticate requests made with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-188">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="3cd27-188">-ValidityPeriod</span></span>
<span data-ttu-id="3cd27-189">將用來從產生 sas 權杖的時間設定其到期時間的有效期間</span><span class="sxs-lookup"><span data-stu-id="3cd27-189">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: TimeSpan
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-190">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3cd27-190">-VaultName</span></span>
<span data-ttu-id="3cd27-191">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="3cd27-191">Vault name.</span></span>
<span data-ttu-id="3cd27-192">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="3cd27-192">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3cd27-193">-確認</span><span class="sxs-lookup"><span data-stu-id="3cd27-193">-Confirm</span></span>
<span data-ttu-id="3cd27-194">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3cd27-194">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cd27-195">-WhatIf</span></span>
<span data-ttu-id="3cd27-196">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3cd27-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cd27-197">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3cd27-197">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd27-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd27-198">CommonParameters</span></span>
<span data-ttu-id="3cd27-199">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3cd27-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd27-200">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3cd27-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd27-201">輸入</span><span class="sxs-lookup"><span data-stu-id="3cd27-201">INPUTS</span></span>

## <span data-ttu-id="3cd27-202">輸出</span><span class="sxs-lookup"><span data-stu-id="3cd27-202">OUTPUTS</span></span>

### <span data-ttu-id="3cd27-203">ManagedStorageSasDefinition 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="3cd27-203">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="3cd27-204">筆記</span><span class="sxs-lookup"><span data-stu-id="3cd27-204">NOTES</span></span>

## <span data-ttu-id="3cd27-205">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cd27-205">RELATED LINKS</span></span>

[<span data-ttu-id="3cd27-206">Azureâ€‹ RM。€‹ Keyâ€‹ Vault</span><span class="sxs-lookup"><span data-stu-id="3cd27-206">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)
