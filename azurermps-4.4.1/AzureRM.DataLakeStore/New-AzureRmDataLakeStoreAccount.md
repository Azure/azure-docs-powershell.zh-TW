---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b05cb9e3789afa905da93642929f65f4965f9b0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626629"
---
# <span data-ttu-id="f669b-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f669b-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="f669b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f669b-102">SYNOPSIS</span></span>
<span data-ttu-id="f669b-103">建立新的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f669b-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f669b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f669b-104">SYNTAX</span></span>

### <span data-ttu-id="f669b-105">使用者或系統獲指派加密 (預設) </span><span class="sxs-lookup"><span data-stu-id="f669b-105">User or System assigned encryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f669b-106">停用加密</span><span class="sxs-lookup"><span data-stu-id="f669b-106">Disable Encryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f669b-107">說明</span><span class="sxs-lookup"><span data-stu-id="f669b-107">DESCRIPTION</span></span>
<span data-ttu-id="f669b-108">**新的-AzureRmDataLakeStoreAccount** Cmdlet 會建立新的 Data Lake store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f669b-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="f669b-109">示例</span><span class="sxs-lookup"><span data-stu-id="f669b-109">EXAMPLES</span></span>

### <span data-ttu-id="f669b-110">範例1：建立帳戶</span><span class="sxs-lookup"><span data-stu-id="f669b-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="f669b-111">這個命令會建立一個名為 ContosoADL 的資料 Lake Store 帳戶，該帳戶是美國東部2的位置。</span><span class="sxs-lookup"><span data-stu-id="f669b-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="f669b-112">參數</span><span class="sxs-lookup"><span data-stu-id="f669b-112">PARAMETERS</span></span>

### <span data-ttu-id="f669b-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="f669b-113">-DefaultGroup</span></span>
<span data-ttu-id="f669b-114">指定 AzureActive 目錄群組的物件識別碼，以做為新檔案和資料夾的預設群組擁有者。</span><span class="sxs-lookup"><span data-stu-id="f669b-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="f669b-115">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="f669b-115">-DisableEncryption</span></span>
<span data-ttu-id="f669b-116">表示帳戶將不會套用任何形式的加密。</span><span class="sxs-lookup"><span data-stu-id="f669b-116">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Encryption
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f669b-117">-加密</span><span class="sxs-lookup"><span data-stu-id="f669b-117">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: User or System assigned encryption
Aliases: 
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f669b-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f669b-118">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f669b-119">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="f669b-119">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f669b-120">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="f669b-120">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f669b-121">-位置</span><span class="sxs-lookup"><span data-stu-id="f669b-121">-Location</span></span>
<span data-ttu-id="f669b-122">指定要用於帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="f669b-122">Specifies the location to use for the account.</span></span>
<span data-ttu-id="f669b-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f669b-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f669b-124">東美國2</span><span class="sxs-lookup"><span data-stu-id="f669b-124">East US 2</span></span>

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

### <span data-ttu-id="f669b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f669b-125">-Name</span></span>
<span data-ttu-id="f669b-126">指定要建立的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f669b-126">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="f669b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f669b-127">-ResourceGroupName</span></span>
<span data-ttu-id="f669b-128">指定包含該帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f669b-128">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="f669b-129">-標記</span><span class="sxs-lookup"><span data-stu-id="f669b-129">-Tags</span></span>
<span data-ttu-id="f669b-130">將標記指定為鍵值對。</span><span class="sxs-lookup"><span data-stu-id="f669b-130">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="f669b-131">您可以使用標籤來識別來自其他 Azure 資源的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f669b-131">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="f669b-132">層級</span><span class="sxs-lookup"><span data-stu-id="f669b-132">-Tier</span></span>
<span data-ttu-id="f669b-133">此帳戶要使用的預期承諾層級。</span><span class="sxs-lookup"><span data-stu-id="f669b-133">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="f669b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f669b-134">-DefaultProfile</span></span>
<span data-ttu-id="f669b-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f669b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f669b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f669b-136">CommonParameters</span></span>
<span data-ttu-id="f669b-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f669b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f669b-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f669b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f669b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f669b-139">INPUTS</span></span>

## <span data-ttu-id="f669b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f669b-140">OUTPUTS</span></span>

### <span data-ttu-id="f669b-141">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f669b-141">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="f669b-142">已建立的帳戶詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f669b-142">The created account details.</span></span>

## <span data-ttu-id="f669b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f669b-143">NOTES</span></span>

## <span data-ttu-id="f669b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f669b-144">RELATED LINKS</span></span>

[<span data-ttu-id="f669b-145">AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f669b-145">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f669b-146">移除-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f669b-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f669b-147">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f669b-147">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f669b-148">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f669b-148">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


