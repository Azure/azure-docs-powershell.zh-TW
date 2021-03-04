---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: ca2db2ece85860c9aeae8e45909cdb5135beaae6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913701"
---
# <span data-ttu-id="ff50e-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff50e-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="ff50e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ff50e-102">SYNOPSIS</span></span>
<span data-ttu-id="ff50e-103">移除儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ff50e-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="ff50e-104">語法</span><span class="sxs-lookup"><span data-stu-id="ff50e-104">SYNTAX</span></span>

### <span data-ttu-id="ff50e-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="ff50e-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff50e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ff50e-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff50e-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="ff50e-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff50e-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="ff50e-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff50e-109">描述</span><span class="sxs-lookup"><span data-stu-id="ff50e-109">DESCRIPTION</span></span>
<span data-ttu-id="ff50e-110">**New-AzRmStorageShare** Cmdlet 會移除儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ff50e-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="ff50e-111">例子</span><span class="sxs-lookup"><span data-stu-id="ff50e-111">EXAMPLES</span></span>

### <span data-ttu-id="ff50e-112">範例 1：移除儲存空間檔案共用與儲存空間帳戶名稱和共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="ff50e-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="ff50e-113">此命令會移除儲存空間檔案共用與儲存空間帳戶名稱和共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="ff50e-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="ff50e-114">範例 2：移除儲存空間帳戶物件和共用名稱稱的儲存空間檔案共用</span><span class="sxs-lookup"><span data-stu-id="ff50e-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="ff50e-115">此命令會移除儲存空間帳戶物件和共用名稱稱的儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ff50e-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="ff50e-116">範例 3：移除儲存帳戶中具有管線的所有儲存空間檔案共用</span><span class="sxs-lookup"><span data-stu-id="ff50e-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="ff50e-117">此命令會移除儲存帳戶中具有管線的所有儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ff50e-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="ff50e-118">參數</span><span class="sxs-lookup"><span data-stu-id="ff50e-118">PARAMETERS</span></span>

### <span data-ttu-id="ff50e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff50e-119">-DefaultProfile</span></span>
<span data-ttu-id="ff50e-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff50e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff50e-121">-強制</span><span class="sxs-lookup"><span data-stu-id="ff50e-121">-Force</span></span>
<span data-ttu-id="ff50e-122">強制移除共用及其中所有內容</span><span class="sxs-lookup"><span data-stu-id="ff50e-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="ff50e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff50e-123">-InputObject</span></span>
<span data-ttu-id="ff50e-124">儲存空間共用物件</span><span class="sxs-lookup"><span data-stu-id="ff50e-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff50e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff50e-125">-Name</span></span>
<span data-ttu-id="ff50e-126">共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="ff50e-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff50e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff50e-127">-PassThru</span></span>
<span data-ttu-id="ff50e-128">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="ff50e-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ff50e-129">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ff50e-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ff50e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff50e-130">-ResourceGroupName</span></span>
<span data-ttu-id="ff50e-131">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ff50e-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff50e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff50e-132">-ResourceId</span></span>
<span data-ttu-id="ff50e-133">輸入檔案共用資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff50e-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="ff50e-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff50e-134">-StorageAccount</span></span>
<span data-ttu-id="ff50e-135">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ff50e-135">Storage account object</span></span>

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

### <span data-ttu-id="ff50e-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ff50e-136">-StorageAccountName</span></span>
<span data-ttu-id="ff50e-137">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ff50e-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="ff50e-138">-確認</span><span class="sxs-lookup"><span data-stu-id="ff50e-138">-Confirm</span></span>
<span data-ttu-id="ff50e-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ff50e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff50e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff50e-140">-WhatIf</span></span>
<span data-ttu-id="ff50e-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff50e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff50e-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff50e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff50e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff50e-143">CommonParameters</span></span>
<span data-ttu-id="ff50e-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ff50e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff50e-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ff50e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff50e-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ff50e-146">INPUTS</span></span>

### <span data-ttu-id="ff50e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="ff50e-147">System.String</span></span>

### <span data-ttu-id="ff50e-148">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff50e-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ff50e-149">Microsoft.Azure.Commands.management.storage.models.PSShare</span><span class="sxs-lookup"><span data-stu-id="ff50e-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="ff50e-150">輸出</span><span class="sxs-lookup"><span data-stu-id="ff50e-150">OUTPUTS</span></span>

### <span data-ttu-id="ff50e-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff50e-151">System.Boolean</span></span>

## <span data-ttu-id="ff50e-152">筆記</span><span class="sxs-lookup"><span data-stu-id="ff50e-152">NOTES</span></span>

## <span data-ttu-id="ff50e-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff50e-153">RELATED LINKS</span></span>
