---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: 2c8980f198dc675e12a9b9c6048a4960c1998f9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915157"
---
# <span data-ttu-id="a2a30-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2a30-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="a2a30-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2a30-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a30-103">獲得儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a2a30-103">Gets a Storage account.</span></span>

## <span data-ttu-id="a2a30-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2a30-104">SYNTAX</span></span>

### <span data-ttu-id="a2a30-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2a30-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2a30-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2a30-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2a30-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2a30-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2a30-108">描述</span><span class="sxs-lookup"><span data-stu-id="a2a30-108">DESCRIPTION</span></span>
<span data-ttu-id="a2a30-109">**Get-AzStorageAccount** Cmdlet 會取得指定的儲存空間帳戶，或資源群組或訂閱中所有的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a2a30-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="a2a30-110">例子</span><span class="sxs-lookup"><span data-stu-id="a2a30-110">EXAMPLES</span></span>

### <span data-ttu-id="a2a30-111">範例 1：取得指定的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="a2a30-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="a2a30-112">此命令會獲得指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a2a30-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="a2a30-113">範例 2：取得資源群組中所有的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="a2a30-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="a2a30-114">此命令會獲得資源群組中所有的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a2a30-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="a2a30-115">範例 3：取得訂閱中所有的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="a2a30-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="a2a30-116">此命令會獲得訂閱中所有的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a2a30-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="a2a30-117">範例 4：取得儲存空間帳戶及其 Blob 還原狀態</span><span class="sxs-lookup"><span data-stu-id="a2a30-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="a2a30-118">此命令會獲得具有 Blob 還原狀態的儲存空間帳戶，並且顯示 Blob 還原狀態。</span><span class="sxs-lookup"><span data-stu-id="a2a30-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="a2a30-119">參數</span><span class="sxs-lookup"><span data-stu-id="a2a30-119">PARAMETERS</span></span>

### <span data-ttu-id="a2a30-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2a30-120">-AsJob</span></span>
<span data-ttu-id="a2a30-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a2a30-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a30-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a30-122">-DefaultProfile</span></span>
<span data-ttu-id="a2a30-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2a30-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2a30-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="a2a30-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="a2a30-125">取得儲存空間帳戶的 BlobRestoreStatus。</span><span class="sxs-lookup"><span data-stu-id="a2a30-125">Get the BlobRestoreStatus of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a30-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="a2a30-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="a2a30-127">取得儲存空間帳戶的 GeoReplicationStats。</span><span class="sxs-lookup"><span data-stu-id="a2a30-127">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a30-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2a30-128">-Name</span></span>
<span data-ttu-id="a2a30-129">指定要取得的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a2a30-129">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a30-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2a30-130">-ResourceGroupName</span></span>
<span data-ttu-id="a2a30-131">指定包含要取得儲存空間帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a2a30-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a30-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a30-132">CommonParameters</span></span>
<span data-ttu-id="a2a30-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2a30-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a30-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a2a30-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a30-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a2a30-135">INPUTS</span></span>

### <span data-ttu-id="a2a30-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a2a30-136">System.String</span></span>

## <span data-ttu-id="a2a30-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a2a30-137">OUTPUTS</span></span>

### <span data-ttu-id="a2a30-138">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2a30-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="a2a30-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a2a30-139">NOTES</span></span>

## <span data-ttu-id="a2a30-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2a30-140">RELATED LINKS</span></span>

[<span data-ttu-id="a2a30-141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2a30-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="a2a30-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2a30-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="a2a30-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2a30-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


