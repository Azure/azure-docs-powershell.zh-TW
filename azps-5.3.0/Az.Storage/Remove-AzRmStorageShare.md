---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436070"
---
# <span data-ttu-id="f2365-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f2365-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="f2365-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2365-102">SYNOPSIS</span></span>
<span data-ttu-id="f2365-103">移除儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="f2365-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="f2365-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2365-104">SYNTAX</span></span>

### <span data-ttu-id="f2365-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="f2365-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2365-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f2365-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2365-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="f2365-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2365-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="f2365-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2365-109">說明</span><span class="sxs-lookup"><span data-stu-id="f2365-109">DESCRIPTION</span></span>
<span data-ttu-id="f2365-110">**新的-AzRmStorageShare** Cmdlet 會移除儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="f2365-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="f2365-111">示例</span><span class="sxs-lookup"><span data-stu-id="f2365-111">EXAMPLES</span></span>

### <span data-ttu-id="f2365-112">範例1：移除儲存空間共用及儲存帳戶名稱和共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="f2365-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="f2365-113">這個命令會移除儲存空間共用的儲存空間帳戶名稱和共用名稱。</span><span class="sxs-lookup"><span data-stu-id="f2365-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="f2365-114">範例2：移除儲存空間共用與儲存帳戶物件及共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="f2365-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="f2365-115">這個命令會移除儲存空間共用的儲存帳戶物件和共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="f2365-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="f2365-116">範例3：移除含管線的儲存空間帳戶中的所有儲存空間共用</span><span class="sxs-lookup"><span data-stu-id="f2365-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="f2365-117">這個命令會移除含管線的儲存空間帳戶中的所有儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="f2365-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="f2365-118">參數</span><span class="sxs-lookup"><span data-stu-id="f2365-118">PARAMETERS</span></span>

### <span data-ttu-id="f2365-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2365-119">-DefaultProfile</span></span>
<span data-ttu-id="f2365-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2365-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2365-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f2365-121">-Force</span></span>
<span data-ttu-id="f2365-122">強制移除共用及其中的所有內容</span><span class="sxs-lookup"><span data-stu-id="f2365-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="f2365-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2365-123">-InputObject</span></span>
<span data-ttu-id="f2365-124">儲存空間份額物件</span><span class="sxs-lookup"><span data-stu-id="f2365-124">Storage Share object</span></span>

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

### <span data-ttu-id="f2365-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2365-125">-Name</span></span>
<span data-ttu-id="f2365-126">共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="f2365-126">Share Name</span></span>

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

### <span data-ttu-id="f2365-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2365-127">-PassThru</span></span>
<span data-ttu-id="f2365-128">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="f2365-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f2365-129">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f2365-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f2365-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2365-130">-ResourceGroupName</span></span>
<span data-ttu-id="f2365-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f2365-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="f2365-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2365-132">-ResourceId</span></span>
<span data-ttu-id="f2365-133">輸入檔案共用資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2365-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="f2365-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f2365-134">-StorageAccount</span></span>
<span data-ttu-id="f2365-135">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="f2365-135">Storage account object</span></span>

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

### <span data-ttu-id="f2365-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f2365-136">-StorageAccountName</span></span>
<span data-ttu-id="f2365-137">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f2365-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="f2365-138">-確認</span><span class="sxs-lookup"><span data-stu-id="f2365-138">-Confirm</span></span>
<span data-ttu-id="f2365-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f2365-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2365-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2365-140">-WhatIf</span></span>
<span data-ttu-id="f2365-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2365-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2365-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2365-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2365-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2365-143">CommonParameters</span></span>
<span data-ttu-id="f2365-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2365-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2365-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2365-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2365-146">輸入</span><span class="sxs-lookup"><span data-stu-id="f2365-146">INPUTS</span></span>

### <span data-ttu-id="f2365-147">System.object</span><span class="sxs-lookup"><span data-stu-id="f2365-147">System.String</span></span>

### <span data-ttu-id="f2365-148">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="f2365-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f2365-149">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="f2365-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f2365-150">輸出</span><span class="sxs-lookup"><span data-stu-id="f2365-150">OUTPUTS</span></span>

### <span data-ttu-id="f2365-151">System.object</span><span class="sxs-lookup"><span data-stu-id="f2365-151">System.Boolean</span></span>

## <span data-ttu-id="f2365-152">筆記</span><span class="sxs-lookup"><span data-stu-id="f2365-152">NOTES</span></span>

## <span data-ttu-id="f2365-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2365-153">RELATED LINKS</span></span>
