---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4bdf13b485486a8e3c40023ea0011d12b21a93b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283568"
---
# <span data-ttu-id="1c286-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1c286-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="1c286-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c286-102">SYNOPSIS</span></span>
<span data-ttu-id="1c286-103">建立新的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1c286-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="1c286-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c286-104">SYNTAX</span></span>

### <span data-ttu-id="1c286-105">UserOrSystemAssignedEncryption (預設) </span><span class="sxs-lookup"><span data-stu-id="1c286-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c286-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="1c286-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c286-107">說明</span><span class="sxs-lookup"><span data-stu-id="1c286-107">DESCRIPTION</span></span>
<span data-ttu-id="1c286-108">**新的-AzDataLakeStoreAccount** Cmdlet 會建立新的 Data Lake store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1c286-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="1c286-109">示例</span><span class="sxs-lookup"><span data-stu-id="1c286-109">EXAMPLES</span></span>

### <span data-ttu-id="1c286-110">範例1：建立帳戶</span><span class="sxs-lookup"><span data-stu-id="1c286-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="1c286-111">這個命令會建立一個名為 ContosoADL 的資料 Lake Store 帳戶，該帳戶是美國東部2的位置。</span><span class="sxs-lookup"><span data-stu-id="1c286-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="1c286-112">參數</span><span class="sxs-lookup"><span data-stu-id="1c286-112">PARAMETERS</span></span>

### <span data-ttu-id="1c286-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="1c286-113">-DefaultGroup</span></span>
<span data-ttu-id="1c286-114">指定 AzureActive 目錄群組的物件識別碼，以做為新檔案和資料夾的預設群組擁有者。</span><span class="sxs-lookup"><span data-stu-id="1c286-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="1c286-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c286-115">-DefaultProfile</span></span>
<span data-ttu-id="1c286-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1c286-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c286-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="1c286-117">-DisableEncryption</span></span>
<span data-ttu-id="1c286-118">表示帳戶將不會套用任何形式的加密。</span><span class="sxs-lookup"><span data-stu-id="1c286-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

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

### <span data-ttu-id="1c286-119">-加密</span><span class="sxs-lookup"><span data-stu-id="1c286-119">-Encryption</span></span>
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

### <span data-ttu-id="1c286-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1c286-120">-KeyName</span></span>
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

### <span data-ttu-id="1c286-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1c286-121">-KeyVaultId</span></span>
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

### <span data-ttu-id="1c286-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="1c286-122">-KeyVersion</span></span>
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

### <span data-ttu-id="1c286-123">-位置</span><span class="sxs-lookup"><span data-stu-id="1c286-123">-Location</span></span>
<span data-ttu-id="1c286-124">指定要用於帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="1c286-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="1c286-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1c286-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1c286-126">東美國2</span><span class="sxs-lookup"><span data-stu-id="1c286-126">East US 2</span></span>

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

### <span data-ttu-id="1c286-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c286-127">-Name</span></span>
<span data-ttu-id="1c286-128">指定要建立的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1c286-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="1c286-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c286-129">-ResourceGroupName</span></span>
<span data-ttu-id="1c286-130">指定包含該帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c286-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="1c286-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c286-131">-Tag</span></span>
<span data-ttu-id="1c286-132">將標記指定為鍵值對。</span><span class="sxs-lookup"><span data-stu-id="1c286-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="1c286-133">您可以使用標籤來識別來自其他 Azure 資源的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1c286-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="1c286-134">層級</span><span class="sxs-lookup"><span data-stu-id="1c286-134">-Tier</span></span>
<span data-ttu-id="1c286-135">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="1c286-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="1c286-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c286-136">CommonParameters</span></span>
<span data-ttu-id="1c286-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c286-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c286-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c286-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c286-139">輸入</span><span class="sxs-lookup"><span data-stu-id="1c286-139">INPUTS</span></span>

### <span data-ttu-id="1c286-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1c286-140">System.String</span></span>

### <span data-ttu-id="1c286-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1c286-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1c286-142">DataLake 為 Nullable "1 [DataLake. EncryptionConfigType，，版本 = 2.0.0.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]）。））））</span><span class="sxs-lookup"><span data-stu-id="1c286-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1c286-143">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="1c286-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1c286-144">DataLake 為 Nullable "1 [DataLake. TierType，，版本 = 2.0.0.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]）。））））</span><span class="sxs-lookup"><span data-stu-id="1c286-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="1c286-145">輸出</span><span class="sxs-lookup"><span data-stu-id="1c286-145">OUTPUTS</span></span>

### <span data-ttu-id="1c286-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1c286-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="1c286-147">筆記</span><span class="sxs-lookup"><span data-stu-id="1c286-147">NOTES</span></span>

## <span data-ttu-id="1c286-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c286-148">RELATED LINKS</span></span>

[<span data-ttu-id="1c286-149">AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1c286-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="1c286-150">移除-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1c286-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="1c286-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1c286-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="1c286-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1c286-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


