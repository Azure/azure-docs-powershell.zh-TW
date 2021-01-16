---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279902"
---
# <span data-ttu-id="6e86e-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="6e86e-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="6e86e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e86e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e86e-103">在儲存空間帳戶中建立或更新指定的物件複製原則。</span><span class="sxs-lookup"><span data-stu-id="6e86e-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="6e86e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e86e-104">SYNTAX</span></span>

### <span data-ttu-id="6e86e-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="6e86e-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e86e-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="6e86e-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e86e-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6e86e-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e86e-108">說明</span><span class="sxs-lookup"><span data-stu-id="6e86e-108">DESCRIPTION</span></span>
<span data-ttu-id="6e86e-109">**AzStorageObjectReplicationPolicy** Cmdlet 會建立或更新儲存空間帳戶中指定的物件複製原則。</span><span class="sxs-lookup"><span data-stu-id="6e86e-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="6e86e-110">示例</span><span class="sxs-lookup"><span data-stu-id="6e86e-110">EXAMPLES</span></span>

### <span data-ttu-id="6e86e-111">範例1：將物件複製原則設定為目的地和來源帳戶。</span><span class="sxs-lookup"><span data-stu-id="6e86e-111">Example 1: Set object replication policy to both destination and source account.</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $destPolicy = Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId default -SourceAccount $srcAccountName  -Rule $rule1,$rule2

PS C:\> $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mysourceaccount" -InputObject $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----                                     
myresourcegroup   mysourceaccount    56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
```

<span data-ttu-id="6e86e-112">這個命令會將物件複製原則設定為目的地和來源帳戶。</span><span class="sxs-lookup"><span data-stu-id="6e86e-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="6e86e-113">首先建立2個物件複製原則規則，並將原則設定為2個規則至 [目的地帳戶]。</span><span class="sxs-lookup"><span data-stu-id="6e86e-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="6e86e-114">然後，將 [物件複製原則] 從 [目的地帳戶] 設定為 [來源帳戶]。</span><span class="sxs-lookup"><span data-stu-id="6e86e-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="6e86e-115">參數</span><span class="sxs-lookup"><span data-stu-id="6e86e-115">PARAMETERS</span></span>

### <span data-ttu-id="6e86e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e86e-116">-DefaultProfile</span></span>
<span data-ttu-id="6e86e-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e86e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e86e-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="6e86e-118">-DestinationAccount</span></span>
<span data-ttu-id="6e86e-119">物件複製原則 DestinationAccount。</span><span class="sxs-lookup"><span data-stu-id="6e86e-119">Object Replication Policy DestinationAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e86e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e86e-120">-InputObject</span></span>
<span data-ttu-id="6e86e-121">要設定為指定帳戶的物件複製原則物件。</span><span class="sxs-lookup"><span data-stu-id="6e86e-121">Object Replication Policy Object to Set to the specified Account.</span></span>

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

### <span data-ttu-id="6e86e-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="6e86e-122">-PolicyId</span></span>
<span data-ttu-id="6e86e-123">物件複製原則識別碼。它應該是 GUID 或「預設」。</span><span class="sxs-lookup"><span data-stu-id="6e86e-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="6e86e-124">如果未輸入 PolicyId，則會使用「預設」，這表示建立新的原則，而建立的原則中將會傳回新原則的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e86e-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e86e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e86e-125">-ResourceGroupName</span></span>
<span data-ttu-id="6e86e-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6e86e-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e86e-127">-規則</span><span class="sxs-lookup"><span data-stu-id="6e86e-127">-Rule</span></span>
<span data-ttu-id="6e86e-128">物件複製原則規則。</span><span class="sxs-lookup"><span data-stu-id="6e86e-128">Object Replication Policy Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule[]
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e86e-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="6e86e-129">-SourceAccount</span></span>
<span data-ttu-id="6e86e-130">物件複製原則 SourceAccount。</span><span class="sxs-lookup"><span data-stu-id="6e86e-130">Object Replication Policy SourceAccount.</span></span>

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

### <span data-ttu-id="6e86e-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6e86e-131">-StorageAccount</span></span>
<span data-ttu-id="6e86e-132">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="6e86e-132">Storage account object</span></span>

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

### <span data-ttu-id="6e86e-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6e86e-133">-StorageAccountName</span></span>
<span data-ttu-id="6e86e-134">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6e86e-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e86e-135">-確認</span><span class="sxs-lookup"><span data-stu-id="6e86e-135">-Confirm</span></span>
<span data-ttu-id="6e86e-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6e86e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e86e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e86e-137">-WhatIf</span></span>
<span data-ttu-id="6e86e-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e86e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e86e-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e86e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e86e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e86e-140">CommonParameters</span></span>
<span data-ttu-id="6e86e-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e86e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e86e-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6e86e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e86e-143">輸入</span><span class="sxs-lookup"><span data-stu-id="6e86e-143">INPUTS</span></span>

### <span data-ttu-id="6e86e-144">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="6e86e-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6e86e-145">PSObjectReplicationPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="6e86e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="6e86e-146">輸出</span><span class="sxs-lookup"><span data-stu-id="6e86e-146">OUTPUTS</span></span>

### <span data-ttu-id="6e86e-147">PSObjectReplicationPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="6e86e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="6e86e-148">筆記</span><span class="sxs-lookup"><span data-stu-id="6e86e-148">NOTES</span></span>

## <span data-ttu-id="6e86e-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e86e-149">RELATED LINKS</span></span>
