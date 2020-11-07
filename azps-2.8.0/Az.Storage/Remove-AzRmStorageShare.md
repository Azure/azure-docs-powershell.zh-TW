---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: 3c4071d11e521476f02cadb7323267f84183510b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793088"
---
# <span data-ttu-id="ce13a-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ce13a-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="ce13a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce13a-102">SYNOPSIS</span></span>
<span data-ttu-id="ce13a-103">移除儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="ce13a-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="ce13a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce13a-104">SYNTAX</span></span>

### <span data-ttu-id="ce13a-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="ce13a-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce13a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ce13a-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce13a-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="ce13a-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce13a-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="ce13a-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce13a-109">說明</span><span class="sxs-lookup"><span data-stu-id="ce13a-109">DESCRIPTION</span></span>
<span data-ttu-id="ce13a-110">**新的-AzRmStorageShare** Cmdlet 會移除儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="ce13a-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="ce13a-111">示例</span><span class="sxs-lookup"><span data-stu-id="ce13a-111">EXAMPLES</span></span>

### <span data-ttu-id="ce13a-112">範例1：移除儲存空間共用及儲存帳戶名稱和共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="ce13a-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="ce13a-113">這個命令會移除儲存空間共用的儲存空間帳戶名稱和共用名稱。</span><span class="sxs-lookup"><span data-stu-id="ce13a-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="ce13a-114">範例2：移除儲存空間共用與儲存帳戶物件及共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="ce13a-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="ce13a-115">這個命令會移除儲存空間共用的儲存帳戶物件和共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="ce13a-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="ce13a-116">範例3：移除含管線的儲存空間帳戶中的所有儲存空間共用</span><span class="sxs-lookup"><span data-stu-id="ce13a-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="ce13a-117">這個命令會移除含管線的儲存空間帳戶中的所有儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="ce13a-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="ce13a-118">參數</span><span class="sxs-lookup"><span data-stu-id="ce13a-118">PARAMETERS</span></span>

### <span data-ttu-id="ce13a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce13a-119">-DefaultProfile</span></span>
<span data-ttu-id="ce13a-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce13a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce13a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ce13a-121">-Force</span></span>
<span data-ttu-id="ce13a-122">強制移除共用及其中的所有內容</span><span class="sxs-lookup"><span data-stu-id="ce13a-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="ce13a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce13a-123">-InputObject</span></span>
<span data-ttu-id="ce13a-124">儲存空間份額物件</span><span class="sxs-lookup"><span data-stu-id="ce13a-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce13a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce13a-125">-Name</span></span>
<span data-ttu-id="ce13a-126">共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="ce13a-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce13a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce13a-127">-PassThru</span></span>
<span data-ttu-id="ce13a-128">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="ce13a-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ce13a-129">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ce13a-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ce13a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce13a-130">-ResourceGroupName</span></span>
<span data-ttu-id="ce13a-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ce13a-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce13a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce13a-132">-ResourceId</span></span>
<span data-ttu-id="ce13a-133">輸入檔案共用資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce13a-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="ce13a-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce13a-134">-StorageAccount</span></span>
<span data-ttu-id="ce13a-135">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ce13a-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce13a-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ce13a-136">-StorageAccountName</span></span>
<span data-ttu-id="ce13a-137">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ce13a-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce13a-138">-確認</span><span class="sxs-lookup"><span data-stu-id="ce13a-138">-Confirm</span></span>
<span data-ttu-id="ce13a-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce13a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce13a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce13a-140">-WhatIf</span></span>
<span data-ttu-id="ce13a-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce13a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce13a-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce13a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce13a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce13a-143">CommonParameters</span></span>
<span data-ttu-id="ce13a-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce13a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce13a-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce13a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce13a-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ce13a-146">INPUTS</span></span>

### <span data-ttu-id="ce13a-147">System.object</span><span class="sxs-lookup"><span data-stu-id="ce13a-147">System.String</span></span>

### <span data-ttu-id="ce13a-148">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ce13a-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ce13a-149">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ce13a-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="ce13a-150">輸出</span><span class="sxs-lookup"><span data-stu-id="ce13a-150">OUTPUTS</span></span>

### <span data-ttu-id="ce13a-151">System.object</span><span class="sxs-lookup"><span data-stu-id="ce13a-151">System.Boolean</span></span>

## <span data-ttu-id="ce13a-152">筆記</span><span class="sxs-lookup"><span data-stu-id="ce13a-152">NOTES</span></span>

## <span data-ttu-id="ce13a-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce13a-153">RELATED LINKS</span></span>
