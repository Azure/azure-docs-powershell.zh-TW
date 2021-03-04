---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 88b142943e37009cf21b35bdaadfd209d1d74c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904241"
---
# <span data-ttu-id="3e4d0-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3e4d0-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="3e4d0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3e4d0-102">SYNOPSIS</span></span>
<span data-ttu-id="3e4d0-103">從 Azure 儲存佇列移除儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="3e4d0-104">語法</span><span class="sxs-lookup"><span data-stu-id="3e4d0-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e4d0-105">描述</span><span class="sxs-lookup"><span data-stu-id="3e4d0-105">DESCRIPTION</span></span>
<span data-ttu-id="3e4d0-106">**Remove-AzStorageQueueStoredAccessPolicy** Cmdlet 會從 Azure 儲存佇列移除儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="3e4d0-107">例子</span><span class="sxs-lookup"><span data-stu-id="3e4d0-107">EXAMPLES</span></span>

### <span data-ttu-id="3e4d0-108">範例 1：從儲存佇列移除儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="3e4d0-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="3e4d0-109">此命令會從名為 MyQueue 的儲存佇列移除名為 Policy04 的存取策略。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="3e4d0-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e4d0-110">PARAMETERS</span></span>

### <span data-ttu-id="3e4d0-111">-內容</span><span class="sxs-lookup"><span data-stu-id="3e4d0-111">-Context</span></span>
<span data-ttu-id="3e4d0-112">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3e4d0-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4d0-114">-DefaultProfile</span></span>
<span data-ttu-id="3e4d0-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e4d0-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e4d0-116">-PassThru</span></span>
<span data-ttu-id="3e4d0-117">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3e4d0-118">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3e4d0-119">-策略</span><span class="sxs-lookup"><span data-stu-id="3e4d0-119">-Policy</span></span>
<span data-ttu-id="3e4d0-120">指定此 Cmdlet 移除的已儲存存取策略名稱。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4d0-121">-佇列</span><span class="sxs-lookup"><span data-stu-id="3e4d0-121">-Queue</span></span>
<span data-ttu-id="3e4d0-122">指定 Azure 儲存佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-122">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4d0-123">-確認</span><span class="sxs-lookup"><span data-stu-id="3e4d0-123">-Confirm</span></span>
<span data-ttu-id="3e4d0-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e4d0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e4d0-125">-WhatIf</span></span>
<span data-ttu-id="3e4d0-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e4d0-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e4d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4d0-128">CommonParameters</span></span>
<span data-ttu-id="3e4d0-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4d0-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3e4d0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4d0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3e4d0-131">INPUTS</span></span>

### <span data-ttu-id="3e4d0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3e4d0-132">System.String</span></span>

### <span data-ttu-id="3e4d0-133">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="3e4d0-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3e4d0-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3e4d0-134">OUTPUTS</span></span>

### <span data-ttu-id="3e4d0-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e4d0-135">System.Boolean</span></span>

## <span data-ttu-id="3e4d0-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3e4d0-136">NOTES</span></span>

## <span data-ttu-id="3e4d0-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e4d0-137">RELATED LINKS</span></span>

[<span data-ttu-id="3e4d0-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3e4d0-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3e4d0-139">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="3e4d0-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3e4d0-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3e4d0-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3e4d0-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3e4d0-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
