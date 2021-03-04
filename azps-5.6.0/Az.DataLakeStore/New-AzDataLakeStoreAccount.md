---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: ee172856bb5935f1a6da4d6dcce92054bd1001e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902086"
---
# <span data-ttu-id="69189-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="69189-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="69189-102">簡介</span><span class="sxs-lookup"><span data-stu-id="69189-102">SYNOPSIS</span></span>
<span data-ttu-id="69189-103">建立新 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="69189-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="69189-104">語法</span><span class="sxs-lookup"><span data-stu-id="69189-104">SYNTAX</span></span>

### <span data-ttu-id="69189-105">UserOrSystemAssignedEncryption (預設) </span><span class="sxs-lookup"><span data-stu-id="69189-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69189-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="69189-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69189-107">描述</span><span class="sxs-lookup"><span data-stu-id="69189-107">DESCRIPTION</span></span>
<span data-ttu-id="69189-108">**New-AzDataLakeStoreAccount** Cmdlet 會建立一個新的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="69189-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="69189-109">例子</span><span class="sxs-lookup"><span data-stu-id="69189-109">EXAMPLES</span></span>

### <span data-ttu-id="69189-110">範例 1：建立帳戶</span><span class="sxs-lookup"><span data-stu-id="69189-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="69189-111">此命令會針對美國東部 2 位置建立名為 ContosoADL 的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="69189-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="69189-112">參數</span><span class="sxs-lookup"><span data-stu-id="69189-112">PARAMETERS</span></span>

### <span data-ttu-id="69189-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="69189-113">-DefaultGroup</span></span>
<span data-ttu-id="69189-114">指定 AzureActive Directory 群組的物件識別碼，做為新檔案和資料夾的預設群組擁有者。</span><span class="sxs-lookup"><span data-stu-id="69189-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="69189-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69189-115">-DefaultProfile</span></span>
<span data-ttu-id="69189-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="69189-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69189-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="69189-117">-DisableEncryption</span></span>
<span data-ttu-id="69189-118">表示該帳戶不會對帳戶進行任何形式的加密。</span><span class="sxs-lookup"><span data-stu-id="69189-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69189-119">-加密</span><span class="sxs-lookup"><span data-stu-id="69189-119">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69189-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="69189-120">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69189-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="69189-121">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69189-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="69189-122">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69189-123">-位置</span><span class="sxs-lookup"><span data-stu-id="69189-123">-Location</span></span>
<span data-ttu-id="69189-124">指定帳戶使用的位置。</span><span class="sxs-lookup"><span data-stu-id="69189-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="69189-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="69189-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69189-126">美國東部 2</span><span class="sxs-lookup"><span data-stu-id="69189-126">East US 2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69189-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="69189-127">-Name</span></span>
<span data-ttu-id="69189-128">指定要建立的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="69189-128">Specifies the name of the account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69189-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69189-129">-ResourceGroupName</span></span>
<span data-ttu-id="69189-130">指定包含該帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="69189-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="69189-131">-標記</span><span class="sxs-lookup"><span data-stu-id="69189-131">-Tag</span></span>
<span data-ttu-id="69189-132">將標記指定為金鑰值組。</span><span class="sxs-lookup"><span data-stu-id="69189-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="69189-133">您可以使用標記來識別來自其他 Azure 資源的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="69189-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69189-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="69189-134">-Tier</span></span>
<span data-ttu-id="69189-135">此帳戶想要使用的承諾層級。</span><span class="sxs-lookup"><span data-stu-id="69189-135">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69189-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69189-136">CommonParameters</span></span>
<span data-ttu-id="69189-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="69189-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69189-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="69189-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69189-139">輸入</span><span class="sxs-lookup"><span data-stu-id="69189-139">INPUTS</span></span>

### <span data-ttu-id="69189-140">System.String</span><span class="sxs-lookup"><span data-stu-id="69189-140">System.String</span></span>

### <span data-ttu-id="69189-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="69189-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="69189-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="69189-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="69189-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="69189-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="69189-144">System.Nullable'1[[Microsoft.Azure.management.DataLake.Store.models.TierType，Microsoft.Azure.management.DataLake.Store， Version=2.0.0.0， Culture=neutral， PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="69189-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="69189-145">輸出</span><span class="sxs-lookup"><span data-stu-id="69189-145">OUTPUTS</span></span>

### <span data-ttu-id="69189-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="69189-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="69189-147">筆記</span><span class="sxs-lookup"><span data-stu-id="69189-147">NOTES</span></span>

## <span data-ttu-id="69189-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="69189-148">RELATED LINKS</span></span>

[<span data-ttu-id="69189-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="69189-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="69189-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="69189-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="69189-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="69189-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="69189-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="69189-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


