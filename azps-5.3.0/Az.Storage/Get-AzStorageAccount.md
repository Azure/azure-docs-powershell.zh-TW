---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286091"
---
# <span data-ttu-id="4f547-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f547-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="4f547-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f547-102">SYNOPSIS</span></span>
<span data-ttu-id="4f547-103">取得儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="4f547-103">Gets a Storage account.</span></span>

## <span data-ttu-id="4f547-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f547-104">SYNTAX</span></span>

### <span data-ttu-id="4f547-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f547-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f547-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f547-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f547-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f547-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f547-108">說明</span><span class="sxs-lookup"><span data-stu-id="4f547-108">DESCRIPTION</span></span>
<span data-ttu-id="4f547-109">**AzStorageAccount** Cmdlet 會取得指定的儲存空間帳戶或資源群組或訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="4f547-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="4f547-110">示例</span><span class="sxs-lookup"><span data-stu-id="4f547-110">EXAMPLES</span></span>

### <span data-ttu-id="4f547-111">範例1：取得指定的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="4f547-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="4f547-112">這個命令會取得指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="4f547-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="4f547-113">範例2：取得資源群組中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="4f547-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="4f547-114">這個命令會取得資源群組中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="4f547-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="4f547-115">範例3：取得訂閱中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="4f547-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="4f547-116">這個命令會取得訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="4f547-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="4f547-117">範例4：取得包含其 blob 還原狀態的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="4f547-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="4f547-118">這個命令會取得含有其 [blob] 還原狀態的儲存空間帳戶，並顯示 [blob 還原] 狀態。</span><span class="sxs-lookup"><span data-stu-id="4f547-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="4f547-119">參數</span><span class="sxs-lookup"><span data-stu-id="4f547-119">PARAMETERS</span></span>

### <span data-ttu-id="4f547-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f547-120">-AsJob</span></span>
<span data-ttu-id="4f547-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4f547-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f547-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f547-122">-DefaultProfile</span></span>
<span data-ttu-id="4f547-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f547-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f547-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="4f547-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="4f547-125">取得儲存空間帳戶的 BlobRestoreStatus。</span><span class="sxs-lookup"><span data-stu-id="4f547-125">Get the BlobRestoreStatus of the Storage account.</span></span>

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

### <span data-ttu-id="4f547-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="4f547-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="4f547-127">取得儲存空間帳戶的 GeoReplicationStats。</span><span class="sxs-lookup"><span data-stu-id="4f547-127">Get the GeoReplicationStats of the Storage account.</span></span>

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

### <span data-ttu-id="4f547-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f547-128">-Name</span></span>
<span data-ttu-id="4f547-129">指定要取得的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4f547-129">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="4f547-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f547-130">-ResourceGroupName</span></span>
<span data-ttu-id="4f547-131">指定包含要取得之儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f547-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="4f547-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f547-132">CommonParameters</span></span>
<span data-ttu-id="4f547-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f547-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f547-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f547-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f547-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4f547-135">INPUTS</span></span>

### <span data-ttu-id="4f547-136">System.object</span><span class="sxs-lookup"><span data-stu-id="4f547-136">System.String</span></span>

## <span data-ttu-id="4f547-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4f547-137">OUTPUTS</span></span>

### <span data-ttu-id="4f547-138">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="4f547-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4f547-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4f547-139">NOTES</span></span>

## <span data-ttu-id="4f547-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f547-140">RELATED LINKS</span></span>

[<span data-ttu-id="4f547-141">新-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f547-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="4f547-142">移除-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f547-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="4f547-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f547-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


