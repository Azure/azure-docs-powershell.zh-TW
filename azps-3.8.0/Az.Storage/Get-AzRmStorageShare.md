---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 2ef5ddb4a260f4749d6ccca6fa964f5e205c4b4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958244"
---
# <span data-ttu-id="ec7b2-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ec7b2-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="ec7b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7b2-103">取得或列出儲存檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="ec7b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec7b2-104">SYNTAX</span></span>

### <span data-ttu-id="ec7b2-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="ec7b2-105">AccountName (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec7b2-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ec7b2-106">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec7b2-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="ec7b2-107">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec7b2-108">說明</span><span class="sxs-lookup"><span data-stu-id="ec7b2-108">DESCRIPTION</span></span>
<span data-ttu-id="ec7b2-109">**AzRmStorageShare** Cmdlet 會取得或列出儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-109">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="ec7b2-110">示例</span><span class="sxs-lookup"><span data-stu-id="ec7b2-110">EXAMPLES</span></span>

### <span data-ttu-id="ec7b2-111">範例1：使用儲存空間帳戶名稱和共用名稱稱來取得儲存檔案共用</span><span class="sxs-lookup"><span data-stu-id="ec7b2-111">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="ec7b2-112">這個命令會透過儲存空間帳戶名稱和共用名稱稱來取得儲存檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-112">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="ec7b2-113">範例2：列出儲存空間帳戶的所有儲存空間份額</span><span class="sxs-lookup"><span data-stu-id="ec7b2-113">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

<span data-ttu-id="ec7b2-114">這個命令會列出儲存空間帳戶名稱的所有儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-114">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="ec7b2-115">範例3：使用儲存空間帳戶物件和容器名稱來取得儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-115">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="ec7b2-116">這個命令會取得含儲存空間帳戶物件和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-116">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="ec7b2-117">參數</span><span class="sxs-lookup"><span data-stu-id="ec7b2-117">PARAMETERS</span></span>

### <span data-ttu-id="ec7b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec7b2-118">-DefaultProfile</span></span>
<span data-ttu-id="ec7b2-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec7b2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec7b2-120">-Name</span></span>
<span data-ttu-id="ec7b2-121">共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="ec7b2-121">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7b2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec7b2-122">-ResourceGroupName</span></span>
<span data-ttu-id="ec7b2-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7b2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec7b2-124">-ResourceId</span></span>
<span data-ttu-id="ec7b2-125">輸入檔案共用資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-125">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7b2-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec7b2-126">-StorageAccount</span></span>
<span data-ttu-id="ec7b2-127">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ec7b2-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7b2-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ec7b2-128">-StorageAccountName</span></span>
<span data-ttu-id="ec7b2-129">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7b2-130">CommonParameters</span></span>
<span data-ttu-id="ec7b2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7b2-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7b2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ec7b2-133">INPUTS</span></span>

### <span data-ttu-id="ec7b2-134">System.object</span><span class="sxs-lookup"><span data-stu-id="ec7b2-134">System.String</span></span>

### <span data-ttu-id="ec7b2-135">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ec7b2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ec7b2-136">OUTPUTS</span></span>

### <span data-ttu-id="ec7b2-137">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ec7b2-137">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="ec7b2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ec7b2-138">NOTES</span></span>

## <span data-ttu-id="ec7b2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec7b2-139">RELATED LINKS</span></span>
