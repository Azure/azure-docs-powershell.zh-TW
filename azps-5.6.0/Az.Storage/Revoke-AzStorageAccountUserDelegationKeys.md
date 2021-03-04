---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: 102f1ebc6152bb521bd1f9c7214a6c48ee61a274
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917881"
---
# <span data-ttu-id="5bae6-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="5bae6-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="5bae6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5bae6-102">SYNOPSIS</span></span>
<span data-ttu-id="5bae6-103">撤銷儲存空間帳戶的所有使用者委派金鑰。</span><span class="sxs-lookup"><span data-stu-id="5bae6-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="5bae6-104">語法</span><span class="sxs-lookup"><span data-stu-id="5bae6-104">SYNTAX</span></span>

### <span data-ttu-id="5bae6-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="5bae6-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bae6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5bae6-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bae6-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="5bae6-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bae6-108">描述</span><span class="sxs-lookup"><span data-stu-id="5bae6-108">DESCRIPTION</span></span>
<span data-ttu-id="5bae6-109">**Revoke-AzStorageAccountUserDelegationKeys** Cmdlet 會撤銷儲存帳戶的所有使用者委派金鑰，因此也會撤銷儲存帳戶的所有 Identity SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="5bae6-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="5bae6-110">例子</span><span class="sxs-lookup"><span data-stu-id="5bae6-110">EXAMPLES</span></span>

### <span data-ttu-id="5bae6-111">範例 1：撤銷儲存帳戶的每個使用者委派金鑰</span><span class="sxs-lookup"><span data-stu-id="5bae6-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="5bae6-112">此範例會撤銷儲存帳戶的所有使用者委派金鑰，因此也會撤銷從使用者委派金鑰產生的所有 Identity SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="5bae6-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="5bae6-113">參數</span><span class="sxs-lookup"><span data-stu-id="5bae6-113">PARAMETERS</span></span>

### <span data-ttu-id="5bae6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bae6-114">-DefaultProfile</span></span>
<span data-ttu-id="5bae6-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5bae6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bae6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bae6-116">-InputObject</span></span>
<span data-ttu-id="5bae6-117">儲存帳戶物件，由 Get_AzStorageAccount，New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="5bae6-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bae6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bae6-118">-PassThru</span></span>
<span data-ttu-id="5bae6-119">一般而言，此 Cmdlet 在成功完成時不會輸出，此參數會強制 Cmdlet 在成功完成 ($true) 值。</span><span class="sxs-lookup"><span data-stu-id="5bae6-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="5bae6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bae6-120">-ResourceGroupName</span></span>
<span data-ttu-id="5bae6-121">包含儲存帳戶資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="5bae6-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="5bae6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bae6-122">-ResourceId</span></span>
<span data-ttu-id="5bae6-123">儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5bae6-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bae6-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5bae6-124">-StorageAccountName</span></span>
<span data-ttu-id="5bae6-125">儲存空間帳戶資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bae6-125">The name of the storage account resource.</span></span>

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

### <span data-ttu-id="5bae6-126">-確認</span><span class="sxs-lookup"><span data-stu-id="5bae6-126">-Confirm</span></span>
<span data-ttu-id="5bae6-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5bae6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bae6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bae6-128">-WhatIf</span></span>
<span data-ttu-id="5bae6-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5bae6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bae6-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5bae6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bae6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bae6-131">CommonParameters</span></span>
<span data-ttu-id="5bae6-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5bae6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bae6-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5bae6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bae6-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5bae6-134">INPUTS</span></span>

### <span data-ttu-id="5bae6-135">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5bae6-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="5bae6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5bae6-136">System.String</span></span>

## <span data-ttu-id="5bae6-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5bae6-137">OUTPUTS</span></span>

### <span data-ttu-id="5bae6-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bae6-138">System.Boolean</span></span>

## <span data-ttu-id="5bae6-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5bae6-139">NOTES</span></span>

## <span data-ttu-id="5bae6-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bae6-140">RELATED LINKS</span></span>
