---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 65a48a000e5b3e4377ca2518992ad80242f9e4d3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957180"
---
# <span data-ttu-id="66c17-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="66c17-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="66c17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66c17-102">SYNOPSIS</span></span>
<span data-ttu-id="66c17-103">取得 Azure Storage Blob 服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="66c17-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="66c17-104">句法</span><span class="sxs-lookup"><span data-stu-id="66c17-104">SYNTAX</span></span>

### <span data-ttu-id="66c17-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="66c17-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c17-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="66c17-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66c17-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="66c17-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66c17-108">說明</span><span class="sxs-lookup"><span data-stu-id="66c17-108">DESCRIPTION</span></span>
<span data-ttu-id="66c17-109">**AzStorageBlobServiceProperty** Cmdlet 會取得 Azure Storage Blob 服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="66c17-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="66c17-110">示例</span><span class="sxs-lookup"><span data-stu-id="66c17-110">EXAMPLES</span></span>

### <span data-ttu-id="66c17-111">範例1：取得指定儲存空間帳戶的 Azure 儲存體 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="66c17-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days 
------------------ ----------------- --------------------- ----------------------------- -------------------------- 
myresourcegroup    mystorageaccount  2018-03-28            False                                                    
```

<span data-ttu-id="66c17-112">這個命令會取得指定儲存空間帳戶的 [Blob 服務] 屬性。</span><span class="sxs-lookup"><span data-stu-id="66c17-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="66c17-113">參數</span><span class="sxs-lookup"><span data-stu-id="66c17-113">PARAMETERS</span></span>

### <span data-ttu-id="66c17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c17-114">-DefaultProfile</span></span>
<span data-ttu-id="66c17-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66c17-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66c17-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c17-116">-ResourceGroupName</span></span>
<span data-ttu-id="66c17-117">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="66c17-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="66c17-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66c17-118">-ResourceId</span></span>
<span data-ttu-id="66c17-119">Blob 服務屬性 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="66c17-119">Blob Service Properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66c17-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="66c17-120">-StorageAccount</span></span>
<span data-ttu-id="66c17-121">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="66c17-121">Storage account object</span></span>

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

### <span data-ttu-id="66c17-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="66c17-122">-StorageAccountName</span></span>
<span data-ttu-id="66c17-123">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="66c17-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c17-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c17-124">CommonParameters</span></span>
<span data-ttu-id="66c17-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66c17-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c17-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66c17-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c17-127">輸入</span><span class="sxs-lookup"><span data-stu-id="66c17-127">INPUTS</span></span>

### <span data-ttu-id="66c17-128">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="66c17-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="66c17-129">System.object</span><span class="sxs-lookup"><span data-stu-id="66c17-129">System.String</span></span>

## <span data-ttu-id="66c17-130">輸出</span><span class="sxs-lookup"><span data-stu-id="66c17-130">OUTPUTS</span></span>

### <span data-ttu-id="66c17-131">PSBlobServiceProperties 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="66c17-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="66c17-132">筆記</span><span class="sxs-lookup"><span data-stu-id="66c17-132">NOTES</span></span>

## <span data-ttu-id="66c17-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="66c17-133">RELATED LINKS</span></span>
