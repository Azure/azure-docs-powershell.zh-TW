---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: cb50a4fd4a50ee2f1d62a3abff338b7a4c77f4cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907226"
---
# <span data-ttu-id="c6ba1-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c6ba1-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="c6ba1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="c6ba1-103">修改 Azure 儲存體檔服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="c6ba1-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6ba1-104">SYNTAX</span></span>

### <span data-ttu-id="c6ba1-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="c6ba1-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6ba1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c6ba1-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6ba1-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="c6ba1-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6ba1-108">描述</span><span class="sxs-lookup"><span data-stu-id="c6ba1-108">DESCRIPTION</span></span>
<span data-ttu-id="c6ba1-109">**Update-AzStorageFileServiceProperty** Cmdlet 會修改 Azure 儲存檔案服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="c6ba1-110">例子</span><span class="sxs-lookup"><span data-stu-id="c6ba1-110">EXAMPLES</span></span>

### <span data-ttu-id="c6ba1-111">範例 1：啟用檔案共用 softdelete</span><span class="sxs-lookup"><span data-stu-id="c6ba1-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName                            : mystorageaccount
ResourceGroupName                             : myresourcegroup
ShareDeleteRetentionPolicy.Enabled            : True
ShareDeleteRetentionPolicy.Days               : 5
```

<span data-ttu-id="c6ba1-112">此命令可讓檔案共用以 5 的保留天數進行刪除</span><span class="sxs-lookup"><span data-stu-id="c6ba1-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="c6ba1-113">參數</span><span class="sxs-lookup"><span data-stu-id="c6ba1-113">PARAMETERS</span></span>

### <span data-ttu-id="c6ba1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6ba1-114">-DefaultProfile</span></span>
<span data-ttu-id="c6ba1-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6ba1-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c6ba1-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="c6ba1-117">設定為 $true，以針對儲存空間帳戶啟用共用刪除保留$false。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ba1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6ba1-118">-ResourceGroupName</span></span>
<span data-ttu-id="c6ba1-119">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6ba1-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6ba1-120">-ResourceId</span></span>
<span data-ttu-id="c6ba1-121">輸入儲存帳戶資源識別碼或檔案服務屬性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6ba1-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="c6ba1-122">-ShareRetentionDays</span></span>
<span data-ttu-id="c6ba1-123">設定共用 DeleteRetentionPolicy 的保留天數。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="c6ba1-124">只有在啟用共用刪除保留原則時，才應設定該值。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-124">The value should only be set when enable share Delete Retention Policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ba1-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6ba1-125">-StorageAccount</span></span>
<span data-ttu-id="c6ba1-126">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="c6ba1-126">Storage account object</span></span>

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

### <span data-ttu-id="c6ba1-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c6ba1-127">-StorageAccountName</span></span>
<span data-ttu-id="c6ba1-128">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="c6ba1-129">-確認</span><span class="sxs-lookup"><span data-stu-id="c6ba1-129">-Confirm</span></span>
<span data-ttu-id="c6ba1-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ba1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6ba1-131">-WhatIf</span></span>
<span data-ttu-id="c6ba1-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6ba1-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6ba1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6ba1-134">CommonParameters</span></span>
<span data-ttu-id="c6ba1-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6ba1-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c6ba1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6ba1-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c6ba1-137">INPUTS</span></span>

### <span data-ttu-id="c6ba1-138">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6ba1-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c6ba1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c6ba1-139">System.String</span></span>

## <span data-ttu-id="c6ba1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c6ba1-140">OUTPUTS</span></span>

### <span data-ttu-id="c6ba1-141">Microsoft.Azure.Commands.management.storage.models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="c6ba1-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="c6ba1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c6ba1-142">NOTES</span></span>

## <span data-ttu-id="c6ba1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6ba1-143">RELATED LINKS</span></span>
