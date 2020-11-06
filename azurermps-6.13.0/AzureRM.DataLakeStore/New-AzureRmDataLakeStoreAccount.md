---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 3a3e2ea1fdac71759de7278ed34666e3a756ccca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443891"
---
# <span data-ttu-id="8101e-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8101e-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="8101e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8101e-102">SYNOPSIS</span></span>
<span data-ttu-id="8101e-103">建立新的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="8101e-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8101e-104">句法</span><span class="sxs-lookup"><span data-stu-id="8101e-104">SYNTAX</span></span>

### <span data-ttu-id="8101e-105">UserOrSystemAssignedEncryption (預設) </span><span class="sxs-lookup"><span data-stu-id="8101e-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8101e-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="8101e-106">DisableEncryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8101e-107">說明</span><span class="sxs-lookup"><span data-stu-id="8101e-107">DESCRIPTION</span></span>
<span data-ttu-id="8101e-108">**新的-AzureRmDataLakeStoreAccount** Cmdlet 會建立新的 Data Lake store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="8101e-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="8101e-109">示例</span><span class="sxs-lookup"><span data-stu-id="8101e-109">EXAMPLES</span></span>

### <span data-ttu-id="8101e-110">範例1：建立帳戶</span><span class="sxs-lookup"><span data-stu-id="8101e-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="8101e-111">這個命令會建立一個名為 ContosoADL 的資料 Lake Store 帳戶，該帳戶是美國東部2的位置。</span><span class="sxs-lookup"><span data-stu-id="8101e-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="8101e-112">參數</span><span class="sxs-lookup"><span data-stu-id="8101e-112">PARAMETERS</span></span>

### <span data-ttu-id="8101e-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="8101e-113">-DefaultGroup</span></span>
<span data-ttu-id="8101e-114">指定 AzureActive 目錄群組的物件識別碼，以做為新檔案和資料夾的預設群組擁有者。</span><span class="sxs-lookup"><span data-stu-id="8101e-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="8101e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8101e-115">-DefaultProfile</span></span>
<span data-ttu-id="8101e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8101e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8101e-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="8101e-117">-DisableEncryption</span></span>
<span data-ttu-id="8101e-118">表示帳戶將不會套用任何形式的加密。</span><span class="sxs-lookup"><span data-stu-id="8101e-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

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

### <span data-ttu-id="8101e-119">-加密</span><span class="sxs-lookup"><span data-stu-id="8101e-119">-Encryption</span></span>
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

### <span data-ttu-id="8101e-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8101e-120">-KeyName</span></span>
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

### <span data-ttu-id="8101e-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="8101e-121">-KeyVaultId</span></span>
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

### <span data-ttu-id="8101e-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="8101e-122">-KeyVersion</span></span>
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

### <span data-ttu-id="8101e-123">-位置</span><span class="sxs-lookup"><span data-stu-id="8101e-123">-Location</span></span>
<span data-ttu-id="8101e-124">指定要用於帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="8101e-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="8101e-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8101e-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8101e-126">東美國2</span><span class="sxs-lookup"><span data-stu-id="8101e-126">East US 2</span></span>

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

### <span data-ttu-id="8101e-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="8101e-127">-Name</span></span>
<span data-ttu-id="8101e-128">指定要建立的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8101e-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="8101e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8101e-129">-ResourceGroupName</span></span>
<span data-ttu-id="8101e-130">指定包含該帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8101e-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="8101e-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="8101e-131">-Tag</span></span>
<span data-ttu-id="8101e-132">將標記指定為鍵值對。</span><span class="sxs-lookup"><span data-stu-id="8101e-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="8101e-133">您可以使用標籤來識別來自其他 Azure 資源的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="8101e-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8101e-134">層級</span><span class="sxs-lookup"><span data-stu-id="8101e-134">-Tier</span></span>
<span data-ttu-id="8101e-135">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="8101e-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="8101e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8101e-136">CommonParameters</span></span>
<span data-ttu-id="8101e-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8101e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8101e-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8101e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8101e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="8101e-139">INPUTS</span></span>

### <span data-ttu-id="8101e-140">System.object</span><span class="sxs-lookup"><span data-stu-id="8101e-140">System.String</span></span>

### <span data-ttu-id="8101e-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8101e-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8101e-142">DataLake 為 Nullable "1 [DataLake. EncryptionConfigType，，版本 = 2.0.0.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]）。））））</span><span class="sxs-lookup"><span data-stu-id="8101e-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8101e-143">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="8101e-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8101e-144">DataLake 為 Nullable "1 [DataLake. TierType，，版本 = 2.0.0.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]）。））））</span><span class="sxs-lookup"><span data-stu-id="8101e-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8101e-145">輸出</span><span class="sxs-lookup"><span data-stu-id="8101e-145">OUTPUTS</span></span>

### <span data-ttu-id="8101e-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8101e-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="8101e-147">筆記</span><span class="sxs-lookup"><span data-stu-id="8101e-147">NOTES</span></span>

## <span data-ttu-id="8101e-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="8101e-148">RELATED LINKS</span></span>

[<span data-ttu-id="8101e-149">AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8101e-149">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="8101e-150">移除-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8101e-150">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="8101e-151">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8101e-151">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="8101e-152">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8101e-152">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


