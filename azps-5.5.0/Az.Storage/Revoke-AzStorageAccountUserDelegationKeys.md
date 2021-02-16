---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133446"
---
# <span data-ttu-id="e46cf-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="e46cf-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="e46cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e46cf-102">SYNOPSIS</span></span>
<span data-ttu-id="e46cf-103">吊銷儲存空間帳戶的所有使用者委派金鑰。</span><span class="sxs-lookup"><span data-stu-id="e46cf-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="e46cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="e46cf-104">SYNTAX</span></span>

### <span data-ttu-id="e46cf-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="e46cf-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e46cf-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e46cf-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e46cf-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e46cf-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e46cf-108">說明</span><span class="sxs-lookup"><span data-stu-id="e46cf-108">DESCRIPTION</span></span>
<span data-ttu-id="e46cf-109">**Revoke AzStorageAccountUserDelegationKeys** Cmdlet 會吊銷儲存空間帳戶的所有使用者委派金鑰，因此儲存帳戶的所有身分識別 SAS 權杖也會被撤銷。</span><span class="sxs-lookup"><span data-stu-id="e46cf-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="e46cf-110">示例</span><span class="sxs-lookup"><span data-stu-id="e46cf-110">EXAMPLES</span></span>

### <span data-ttu-id="e46cf-111">範例1：撤銷儲存空間帳戶的所有使用者委派金鑰</span><span class="sxs-lookup"><span data-stu-id="e46cf-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="e46cf-112">這個範例會吊銷儲存空間帳戶的所有使用者委派金鑰，因此也會撤銷從使用者委派金鑰產生的所有身分識別 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="e46cf-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="e46cf-113">參數</span><span class="sxs-lookup"><span data-stu-id="e46cf-113">PARAMETERS</span></span>

### <span data-ttu-id="e46cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46cf-114">-DefaultProfile</span></span>
<span data-ttu-id="e46cf-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e46cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e46cf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e46cf-116">-InputObject</span></span>
<span data-ttu-id="e46cf-117">Get_AzStorageAccount AzStorageAccount 的儲存帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="e46cf-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

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

### <span data-ttu-id="e46cf-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e46cf-118">-PassThru</span></span>
<span data-ttu-id="e46cf-119">這個 Cmdlet 在成功完成時不會傳回輸出，此參數會強制 Cmdlet 在成功完成時，傳回 $true)  (的值。</span><span class="sxs-lookup"><span data-stu-id="e46cf-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="e46cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e46cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="e46cf-121">包含儲存空間帳戶資源的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e46cf-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="e46cf-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e46cf-122">-ResourceId</span></span>
<span data-ttu-id="e46cf-123">儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e46cf-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="e46cf-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e46cf-124">-StorageAccountName</span></span>
<span data-ttu-id="e46cf-125">儲存空間帳戶資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e46cf-125">The name of the storage account resource.</span></span>

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

### <span data-ttu-id="e46cf-126">-確認</span><span class="sxs-lookup"><span data-stu-id="e46cf-126">-Confirm</span></span>
<span data-ttu-id="e46cf-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e46cf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e46cf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e46cf-128">-WhatIf</span></span>
<span data-ttu-id="e46cf-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e46cf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e46cf-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e46cf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e46cf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46cf-131">CommonParameters</span></span>
<span data-ttu-id="e46cf-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e46cf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46cf-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e46cf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46cf-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e46cf-134">INPUTS</span></span>

### <span data-ttu-id="e46cf-135">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="e46cf-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e46cf-136">System.object</span><span class="sxs-lookup"><span data-stu-id="e46cf-136">System.String</span></span>

## <span data-ttu-id="e46cf-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e46cf-137">OUTPUTS</span></span>

### <span data-ttu-id="e46cf-138">System.object</span><span class="sxs-lookup"><span data-stu-id="e46cf-138">System.Boolean</span></span>

## <span data-ttu-id="e46cf-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e46cf-139">NOTES</span></span>

## <span data-ttu-id="e46cf-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e46cf-140">RELATED LINKS</span></span>
