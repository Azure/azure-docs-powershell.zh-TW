---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 083114668fe46da6fb2ca8ba47bc540067539532
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795088"
---
# <span data-ttu-id="cda5d-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cda5d-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="cda5d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cda5d-102">SYNOPSIS</span></span>
<span data-ttu-id="cda5d-103">建立 Azure 儲存空間資料表的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="cda5d-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="cda5d-104">句法</span><span class="sxs-lookup"><span data-stu-id="cda5d-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cda5d-105">說明</span><span class="sxs-lookup"><span data-stu-id="cda5d-105">DESCRIPTION</span></span>
<span data-ttu-id="cda5d-106">**新的-AzStorageTableStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間資料表建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="cda5d-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="cda5d-107">示例</span><span class="sxs-lookup"><span data-stu-id="cda5d-107">EXAMPLES</span></span>

### <span data-ttu-id="cda5d-108">範例1：在資料表中建立儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="cda5d-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="cda5d-109">這個命令會在名為 MyTable 的存儲資料表中，建立名為 Policy02 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="cda5d-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="cda5d-110">參數</span><span class="sxs-lookup"><span data-stu-id="cda5d-110">PARAMETERS</span></span>

### <span data-ttu-id="cda5d-111">-內容</span><span class="sxs-lookup"><span data-stu-id="cda5d-111">-Context</span></span>
<span data-ttu-id="cda5d-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="cda5d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cda5d-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cda5d-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cda5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda5d-114">-DefaultProfile</span></span>
<span data-ttu-id="cda5d-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cda5d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cda5d-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cda5d-116">-ExpiryTime</span></span>
<span data-ttu-id="cda5d-117">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="cda5d-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="cda5d-118">-許可權</span><span class="sxs-lookup"><span data-stu-id="cda5d-118">-Permission</span></span>
<span data-ttu-id="cda5d-119">指定儲存的存取原則中的許可權來存取儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="cda5d-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="cda5d-120">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="cda5d-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="cda5d-121">-原則</span><span class="sxs-lookup"><span data-stu-id="cda5d-121">-Policy</span></span>
<span data-ttu-id="cda5d-122">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="cda5d-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="cda5d-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cda5d-123">-StartTime</span></span>
<span data-ttu-id="cda5d-124">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="cda5d-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="cda5d-125">-資料表</span><span class="sxs-lookup"><span data-stu-id="cda5d-125">-Table</span></span>
<span data-ttu-id="cda5d-126">指定 Azure 儲存空間資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="cda5d-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="cda5d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda5d-127">CommonParameters</span></span>
<span data-ttu-id="cda5d-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cda5d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda5d-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cda5d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda5d-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cda5d-130">INPUTS</span></span>

### <span data-ttu-id="cda5d-131">System.object</span><span class="sxs-lookup"><span data-stu-id="cda5d-131">System.String</span></span>

### <span data-ttu-id="cda5d-132">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="cda5d-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cda5d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cda5d-133">OUTPUTS</span></span>

### <span data-ttu-id="cda5d-134">System.object</span><span class="sxs-lookup"><span data-stu-id="cda5d-134">System.String</span></span>

## <span data-ttu-id="cda5d-135">筆記</span><span class="sxs-lookup"><span data-stu-id="cda5d-135">NOTES</span></span>

## <span data-ttu-id="cda5d-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cda5d-136">RELATED LINKS</span></span>

[<span data-ttu-id="cda5d-137">AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cda5d-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="cda5d-138">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="cda5d-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="cda5d-139">移除-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cda5d-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="cda5d-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cda5d-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

