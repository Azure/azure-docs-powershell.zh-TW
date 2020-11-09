---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287695"
---
# <span data-ttu-id="cddf0-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cddf0-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="cddf0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cddf0-102">SYNOPSIS</span></span>
<span data-ttu-id="cddf0-103">修改 Azure 儲存空間服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="cddf0-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="cddf0-104">句法</span><span class="sxs-lookup"><span data-stu-id="cddf0-104">SYNTAX</span></span>

### <span data-ttu-id="cddf0-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="cddf0-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddf0-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cddf0-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cddf0-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="cddf0-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cddf0-108">說明</span><span class="sxs-lookup"><span data-stu-id="cddf0-108">DESCRIPTION</span></span>
<span data-ttu-id="cddf0-109">**AzStorageFileServiceProperty** Cmdlet 會修改 Azure 儲存空間服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="cddf0-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="cddf0-110">示例</span><span class="sxs-lookup"><span data-stu-id="cddf0-110">EXAMPLES</span></span>

### <span data-ttu-id="cddf0-111">範例1：啟用檔案共用 softdelete</span><span class="sxs-lookup"><span data-stu-id="cddf0-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="cddf0-112">這個命令啟用檔案共用 softdelete 刪除，保留天數為5</span><span class="sxs-lookup"><span data-stu-id="cddf0-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="cddf0-113">參數</span><span class="sxs-lookup"><span data-stu-id="cddf0-113">PARAMETERS</span></span>

### <span data-ttu-id="cddf0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cddf0-114">-DefaultProfile</span></span>
<span data-ttu-id="cddf0-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cddf0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cddf0-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cddf0-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="cddf0-117">將儲存帳戶的 [刪除保留原則] 設定為 [$true，停用 [共用刪除保留原則] 設定為 [$false]。</span><span class="sxs-lookup"><span data-stu-id="cddf0-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

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

### <span data-ttu-id="cddf0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cddf0-118">-ResourceGroupName</span></span>
<span data-ttu-id="cddf0-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cddf0-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="cddf0-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cddf0-120">-ResourceId</span></span>
<span data-ttu-id="cddf0-121">輸入儲存空間帳戶資源識別碼，或 [檔案服務] 屬性 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cddf0-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="cddf0-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="cddf0-122">-ShareRetentionDays</span></span>
<span data-ttu-id="cddf0-123">設定 [共用 DeleteRetentionPolicy] 的保留天數。</span><span class="sxs-lookup"><span data-stu-id="cddf0-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="cddf0-124">只有在啟用共用刪除保留原則時，才應設定此值。</span><span class="sxs-lookup"><span data-stu-id="cddf0-124">The value should only be set when enable share Delete Retention Policy.</span></span>

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

### <span data-ttu-id="cddf0-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cddf0-125">-StorageAccount</span></span>
<span data-ttu-id="cddf0-126">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="cddf0-126">Storage account object</span></span>

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

### <span data-ttu-id="cddf0-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cddf0-127">-StorageAccountName</span></span>
<span data-ttu-id="cddf0-128">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cddf0-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="cddf0-129">-確認</span><span class="sxs-lookup"><span data-stu-id="cddf0-129">-Confirm</span></span>
<span data-ttu-id="cddf0-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cddf0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cddf0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cddf0-131">-WhatIf</span></span>
<span data-ttu-id="cddf0-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cddf0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cddf0-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cddf0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cddf0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cddf0-134">CommonParameters</span></span>
<span data-ttu-id="cddf0-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cddf0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cddf0-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cddf0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cddf0-137">輸入</span><span class="sxs-lookup"><span data-stu-id="cddf0-137">INPUTS</span></span>

### <span data-ttu-id="cddf0-138">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="cddf0-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="cddf0-139">System.object</span><span class="sxs-lookup"><span data-stu-id="cddf0-139">System.String</span></span>

## <span data-ttu-id="cddf0-140">輸出</span><span class="sxs-lookup"><span data-stu-id="cddf0-140">OUTPUTS</span></span>

### <span data-ttu-id="cddf0-141">PSFileServiceProperties 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="cddf0-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="cddf0-142">筆記</span><span class="sxs-lookup"><span data-stu-id="cddf0-142">NOTES</span></span>

## <span data-ttu-id="cddf0-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="cddf0-143">RELATED LINKS</span></span>
