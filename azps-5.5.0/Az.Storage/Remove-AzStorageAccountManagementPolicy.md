---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6f4907f9ee94c05161fa602fc5cefd0ead4f6224
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134395"
---
# <span data-ttu-id="0a4ff-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0a4ff-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="0a4ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="0a4ff-103">移除 Azure 儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="0a4ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a4ff-104">SYNTAX</span></span>

### <span data-ttu-id="0a4ff-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="0a4ff-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a4ff-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0a4ff-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a4ff-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="0a4ff-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a4ff-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="0a4ff-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a4ff-109">說明</span><span class="sxs-lookup"><span data-stu-id="0a4ff-109">DESCRIPTION</span></span>
<span data-ttu-id="0a4ff-110">**AzStorageAccountManagementPolicy** Cmdlet 會移除 Azure 儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="0a4ff-111">示例</span><span class="sxs-lookup"><span data-stu-id="0a4ff-111">EXAMPLES</span></span>

### <span data-ttu-id="0a4ff-112">範例1：移除儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="0a4ff-113">這個命令會移除儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="0a4ff-114">參數</span><span class="sxs-lookup"><span data-stu-id="0a4ff-114">PARAMETERS</span></span>

### <span data-ttu-id="0a4ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a4ff-115">-DefaultProfile</span></span>
<span data-ttu-id="0a4ff-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a4ff-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a4ff-117">-InputObject</span></span>
<span data-ttu-id="0a4ff-118">要移除的管理物件</span><span class="sxs-lookup"><span data-stu-id="0a4ff-118">Management Object to Remove</span></span>

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

### <span data-ttu-id="0a4ff-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a4ff-119">-PassThru</span></span>
<span data-ttu-id="0a4ff-120">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="0a4ff-121">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="0a4ff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a4ff-122">-ResourceGroupName</span></span>
<span data-ttu-id="0a4ff-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="0a4ff-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a4ff-124">-StorageAccount</span></span>
<span data-ttu-id="0a4ff-125">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="0a4ff-125">Storage account object</span></span>

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

### <span data-ttu-id="0a4ff-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0a4ff-126">-StorageAccountName</span></span>
<span data-ttu-id="0a4ff-127">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="0a4ff-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="0a4ff-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="0a4ff-129">儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-129">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="0a4ff-130">-確認</span><span class="sxs-lookup"><span data-stu-id="0a4ff-130">-Confirm</span></span>
<span data-ttu-id="0a4ff-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a4ff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a4ff-132">-WhatIf</span></span>
<span data-ttu-id="0a4ff-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a4ff-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a4ff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a4ff-135">CommonParameters</span></span>
<span data-ttu-id="0a4ff-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a4ff-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a4ff-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a4ff-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0a4ff-138">INPUTS</span></span>

### <span data-ttu-id="0a4ff-139">System.object</span><span class="sxs-lookup"><span data-stu-id="0a4ff-139">System.String</span></span>

## <span data-ttu-id="0a4ff-140">輸出</span><span class="sxs-lookup"><span data-stu-id="0a4ff-140">OUTPUTS</span></span>

### <span data-ttu-id="0a4ff-141">System.object</span><span class="sxs-lookup"><span data-stu-id="0a4ff-141">System.Boolean</span></span>

## <span data-ttu-id="0a4ff-142">筆記</span><span class="sxs-lookup"><span data-stu-id="0a4ff-142">NOTES</span></span>

## <span data-ttu-id="0a4ff-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a4ff-143">RELATED LINKS</span></span>
