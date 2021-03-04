---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 671a83ee392f59dc27cff6cc34eeb7df054b3fbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915026"
---
# <span data-ttu-id="09019-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="09019-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="09019-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09019-102">SYNOPSIS</span></span>
<span data-ttu-id="09019-103">移除 Azure 儲存體帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="09019-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="09019-104">語法</span><span class="sxs-lookup"><span data-stu-id="09019-104">SYNTAX</span></span>

### <span data-ttu-id="09019-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="09019-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09019-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="09019-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09019-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="09019-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09019-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="09019-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09019-109">描述</span><span class="sxs-lookup"><span data-stu-id="09019-109">DESCRIPTION</span></span>
<span data-ttu-id="09019-110">**Remove-AzStorageAccountManagementPolicy** Cmdlet 會移除 Azure 儲存體帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="09019-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="09019-111">例子</span><span class="sxs-lookup"><span data-stu-id="09019-111">EXAMPLES</span></span>

### <span data-ttu-id="09019-112">範例 1：移除儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="09019-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="09019-113">此命令會移除儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="09019-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="09019-114">參數</span><span class="sxs-lookup"><span data-stu-id="09019-114">PARAMETERS</span></span>

### <span data-ttu-id="09019-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09019-115">-DefaultProfile</span></span>
<span data-ttu-id="09019-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="09019-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09019-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09019-117">-InputObject</span></span>
<span data-ttu-id="09019-118">要移除的管理物件</span><span class="sxs-lookup"><span data-stu-id="09019-118">Management Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: PolicyObject
Aliases: ManagementPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09019-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09019-119">-PassThru</span></span>
<span data-ttu-id="09019-120">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="09019-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="09019-121">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="09019-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="09019-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09019-122">-ResourceGroupName</span></span>
<span data-ttu-id="09019-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="09019-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="09019-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="09019-124">-StorageAccount</span></span>
<span data-ttu-id="09019-125">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="09019-125">Storage account object</span></span>

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

### <span data-ttu-id="09019-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="09019-126">-StorageAccountName</span></span>
<span data-ttu-id="09019-127">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="09019-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="09019-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="09019-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="09019-129">儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="09019-129">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09019-130">-確認</span><span class="sxs-lookup"><span data-stu-id="09019-130">-Confirm</span></span>
<span data-ttu-id="09019-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="09019-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09019-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09019-132">-WhatIf</span></span>
<span data-ttu-id="09019-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09019-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09019-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09019-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09019-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09019-135">CommonParameters</span></span>
<span data-ttu-id="09019-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09019-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09019-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="09019-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09019-138">輸入</span><span class="sxs-lookup"><span data-stu-id="09019-138">INPUTS</span></span>

### <span data-ttu-id="09019-139">System.String</span><span class="sxs-lookup"><span data-stu-id="09019-139">System.String</span></span>

## <span data-ttu-id="09019-140">輸出</span><span class="sxs-lookup"><span data-stu-id="09019-140">OUTPUTS</span></span>

### <span data-ttu-id="09019-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="09019-141">System.Boolean</span></span>

## <span data-ttu-id="09019-142">筆記</span><span class="sxs-lookup"><span data-stu-id="09019-142">NOTES</span></span>

## <span data-ttu-id="09019-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="09019-143">RELATED LINKS</span></span>
