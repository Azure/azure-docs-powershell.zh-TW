---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137250"
---
# <span data-ttu-id="f696d-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="f696d-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="f696d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f696d-102">SYNOPSIS</span></span>
<span data-ttu-id="f696d-103">從儲存空間帳戶移除指定的物件複製原則。</span><span class="sxs-lookup"><span data-stu-id="f696d-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="f696d-104">句法</span><span class="sxs-lookup"><span data-stu-id="f696d-104">SYNTAX</span></span>

### <span data-ttu-id="f696d-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="f696d-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f696d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f696d-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f696d-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="f696d-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f696d-108">說明</span><span class="sxs-lookup"><span data-stu-id="f696d-108">DESCRIPTION</span></span>
<span data-ttu-id="f696d-109">**AzStorageObjectReplicationPolicy** Cmdlet 會從儲存空間帳戶中移除指定的物件複製原則。</span><span class="sxs-lookup"><span data-stu-id="f696d-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="f696d-110">示例</span><span class="sxs-lookup"><span data-stu-id="f696d-110">EXAMPLES</span></span>

### <span data-ttu-id="f696d-111">範例1：從儲存空間帳戶中移除特定 policyId 的物件複製原則。</span><span class="sxs-lookup"><span data-stu-id="f696d-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="f696d-112">這個命令會從儲存空間帳戶中移除含有特定 policyId 的物件複製原則。</span><span class="sxs-lookup"><span data-stu-id="f696d-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="f696d-113">參數</span><span class="sxs-lookup"><span data-stu-id="f696d-113">PARAMETERS</span></span>

### <span data-ttu-id="f696d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f696d-114">-DefaultProfile</span></span>
<span data-ttu-id="f696d-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f696d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f696d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f696d-116">-InputObject</span></span>
<span data-ttu-id="f696d-117">要刪除的物件複製原則物件。</span><span class="sxs-lookup"><span data-stu-id="f696d-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="f696d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f696d-118">-PassThru</span></span>
<span data-ttu-id="f696d-119">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="f696d-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f696d-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="f696d-120">-PolicyId</span></span>
<span data-ttu-id="f696d-121">物件複製原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="f696d-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="f696d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f696d-122">-ResourceGroupName</span></span>
<span data-ttu-id="f696d-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f696d-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="f696d-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f696d-124">-StorageAccount</span></span>
<span data-ttu-id="f696d-125">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="f696d-125">Storage account object</span></span>

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

### <span data-ttu-id="f696d-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f696d-126">-StorageAccountName</span></span>
<span data-ttu-id="f696d-127">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f696d-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="f696d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="f696d-128">-Confirm</span></span>
<span data-ttu-id="f696d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f696d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f696d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f696d-130">-WhatIf</span></span>
<span data-ttu-id="f696d-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f696d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f696d-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f696d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f696d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f696d-133">CommonParameters</span></span>
<span data-ttu-id="f696d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f696d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f696d-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f696d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f696d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="f696d-136">INPUTS</span></span>

### <span data-ttu-id="f696d-137">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="f696d-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f696d-138">PSObjectReplicationPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="f696d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="f696d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f696d-139">OUTPUTS</span></span>

### <span data-ttu-id="f696d-140">System.object</span><span class="sxs-lookup"><span data-stu-id="f696d-140">System.Boolean</span></span>

## <span data-ttu-id="f696d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f696d-141">NOTES</span></span>

## <span data-ttu-id="f696d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f696d-142">RELATED LINKS</span></span>