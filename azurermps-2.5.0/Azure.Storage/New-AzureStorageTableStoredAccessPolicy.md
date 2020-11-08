---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 21e289ce0a8e7ca2d430d64ab9cc75bfd0c1a3ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802154"
---
# <span data-ttu-id="ff195-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff195-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="ff195-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff195-102">SYNOPSIS</span></span>
<span data-ttu-id="ff195-103">建立 Azure 儲存空間資料表的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="ff195-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff195-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff195-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff195-105">說明</span><span class="sxs-lookup"><span data-stu-id="ff195-105">DESCRIPTION</span></span>
<span data-ttu-id="ff195-106">**新的-AzureStorageTableStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間資料表建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="ff195-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="ff195-107">示例</span><span class="sxs-lookup"><span data-stu-id="ff195-107">EXAMPLES</span></span>

### <span data-ttu-id="ff195-108">範例1：在資料表中建立儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="ff195-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="ff195-109">這個命令會在名為 MyTable 的存儲資料表中，建立名為 Policy02 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="ff195-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="ff195-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff195-110">PARAMETERS</span></span>

### <span data-ttu-id="ff195-111">-內容</span><span class="sxs-lookup"><span data-stu-id="ff195-111">-Context</span></span>
<span data-ttu-id="ff195-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="ff195-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ff195-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff195-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff195-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff195-114">-DefaultProfile</span></span>
<span data-ttu-id="ff195-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff195-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff195-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ff195-116">-ExpiryTime</span></span>
<span data-ttu-id="ff195-117">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="ff195-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="ff195-118">-許可權</span><span class="sxs-lookup"><span data-stu-id="ff195-118">-Permission</span></span>
<span data-ttu-id="ff195-119">指定儲存的存取原則中的許可權來存取儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="ff195-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="ff195-120">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="ff195-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ff195-121">-原則</span><span class="sxs-lookup"><span data-stu-id="ff195-121">-Policy</span></span>
<span data-ttu-id="ff195-122">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff195-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff195-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ff195-123">-StartTime</span></span>
<span data-ttu-id="ff195-124">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="ff195-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="ff195-125">-資料表</span><span class="sxs-lookup"><span data-stu-id="ff195-125">-Table</span></span>
<span data-ttu-id="ff195-126">指定 Azure 儲存空間資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="ff195-126">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff195-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff195-127">CommonParameters</span></span>
<span data-ttu-id="ff195-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff195-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff195-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff195-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff195-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ff195-130">INPUTS</span></span>

### <span data-ttu-id="ff195-131">System.object</span><span class="sxs-lookup"><span data-stu-id="ff195-131">System.String</span></span>

### <span data-ttu-id="ff195-132">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="ff195-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ff195-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ff195-133">OUTPUTS</span></span>

### <span data-ttu-id="ff195-134">System.object</span><span class="sxs-lookup"><span data-stu-id="ff195-134">System.String</span></span>

## <span data-ttu-id="ff195-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ff195-135">NOTES</span></span>

## <span data-ttu-id="ff195-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff195-136">RELATED LINKS</span></span>

[<span data-ttu-id="ff195-137">AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff195-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ff195-138">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ff195-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ff195-139">移除-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff195-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ff195-140">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff195-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

