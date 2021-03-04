---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 17ccb6e41e826ffd6b522c353ff51cf360b5af0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904253"
---
# <span data-ttu-id="600ca-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="600ca-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="600ca-102">簡介</span><span class="sxs-lookup"><span data-stu-id="600ca-102">SYNOPSIS</span></span>
<span data-ttu-id="600ca-103">從儲存空間帳戶移除指定的物件複寫原則。</span><span class="sxs-lookup"><span data-stu-id="600ca-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="600ca-104">語法</span><span class="sxs-lookup"><span data-stu-id="600ca-104">SYNTAX</span></span>

### <span data-ttu-id="600ca-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="600ca-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="600ca-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="600ca-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600ca-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="600ca-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="600ca-108">描述</span><span class="sxs-lookup"><span data-stu-id="600ca-108">DESCRIPTION</span></span>
<span data-ttu-id="600ca-109">**Remove-AzStorageObjectReplicationPolicy** Cmdlet 會從儲存帳戶移除指定的物件複寫原則。</span><span class="sxs-lookup"><span data-stu-id="600ca-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="600ca-110">例子</span><span class="sxs-lookup"><span data-stu-id="600ca-110">EXAMPLES</span></span>

### <span data-ttu-id="600ca-111">範例 1：從儲存帳戶移除具有特定 policyId 的物件複寫原則。</span><span class="sxs-lookup"><span data-stu-id="600ca-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="600ca-112">此命令會從儲存帳戶移除具有特定 policyId 的物件複寫原則。</span><span class="sxs-lookup"><span data-stu-id="600ca-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="600ca-113">參數</span><span class="sxs-lookup"><span data-stu-id="600ca-113">PARAMETERS</span></span>

### <span data-ttu-id="600ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600ca-114">-DefaultProfile</span></span>
<span data-ttu-id="600ca-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="600ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="600ca-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="600ca-116">-InputObject</span></span>
<span data-ttu-id="600ca-117">要刪除的物件複寫原則物件。</span><span class="sxs-lookup"><span data-stu-id="600ca-117">Object Replication Policy object to Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="600ca-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="600ca-118">-PassThru</span></span>
<span data-ttu-id="600ca-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="600ca-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="600ca-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="600ca-120">-PolicyId</span></span>
<span data-ttu-id="600ca-121">物件複寫原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="600ca-121">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="600ca-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="600ca-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="600ca-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="600ca-124">-StorageAccount</span></span>
<span data-ttu-id="600ca-125">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="600ca-125">Storage account object</span></span>

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

### <span data-ttu-id="600ca-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="600ca-126">-StorageAccountName</span></span>
<span data-ttu-id="600ca-127">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="600ca-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="600ca-128">-確認</span><span class="sxs-lookup"><span data-stu-id="600ca-128">-Confirm</span></span>
<span data-ttu-id="600ca-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="600ca-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="600ca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="600ca-130">-WhatIf</span></span>
<span data-ttu-id="600ca-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="600ca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="600ca-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="600ca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="600ca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600ca-133">CommonParameters</span></span>
<span data-ttu-id="600ca-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="600ca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600ca-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="600ca-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600ca-136">輸入</span><span class="sxs-lookup"><span data-stu-id="600ca-136">INPUTS</span></span>

### <span data-ttu-id="600ca-137">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="600ca-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="600ca-138">Microsoft.Azure.Commands.management.storage.models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="600ca-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="600ca-139">輸出</span><span class="sxs-lookup"><span data-stu-id="600ca-139">OUTPUTS</span></span>

### <span data-ttu-id="600ca-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="600ca-140">System.Boolean</span></span>

## <span data-ttu-id="600ca-141">筆記</span><span class="sxs-lookup"><span data-stu-id="600ca-141">NOTES</span></span>

## <span data-ttu-id="600ca-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="600ca-142">RELATED LINKS</span></span>
