---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: aaf020d61941057dd0dabac849adb37197e02882
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910769"
---
# <span data-ttu-id="59327-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="59327-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="59327-102">簡介</span><span class="sxs-lookup"><span data-stu-id="59327-102">SYNOPSIS</span></span>
<span data-ttu-id="59327-103">在批次處理計算節點上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="59327-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="59327-104">語法</span><span class="sxs-lookup"><span data-stu-id="59327-104">SYNTAX</span></span>

### <span data-ttu-id="59327-105">Id</span><span class="sxs-lookup"><span data-stu-id="59327-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59327-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="59327-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59327-107">描述</span><span class="sxs-lookup"><span data-stu-id="59327-107">DESCRIPTION</span></span>
<span data-ttu-id="59327-108">**New-AzBatchComputeNodeUser** Cmdlet 在 Azure Batch 計算節點上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="59327-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="59327-109">例子</span><span class="sxs-lookup"><span data-stu-id="59327-109">EXAMPLES</span></span>

### <span data-ttu-id="59327-110">範例 1：建立具有系統管理認證之使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="59327-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="59327-111">此命令在具有 ID ComputeNode01 的計算節點上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="59327-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="59327-112">節點位於具有 ID MyPool01 的集中。</span><span class="sxs-lookup"><span data-stu-id="59327-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="59327-113">使用者名稱為 TestUser、密碼為密碼、帳戶會在七天后過期，且帳戶具有系統管理認證。</span><span class="sxs-lookup"><span data-stu-id="59327-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="59327-114">範例 2：使用管線在計算節點上建立使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="59327-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="59327-115">此命令會使用 **Get-AzBatchComputeNode** Cmdlet 取得名為 ComputeNode01 的計算節點。</span><span class="sxs-lookup"><span data-stu-id="59327-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="59327-116">該節點位於具有 ID MyPool01 的集中。</span><span class="sxs-lookup"><span data-stu-id="59327-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="59327-117">該命令會使用管線運算子，將計算節點傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59327-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="59327-118">該命令會建立一個使用者帳戶，該帳戶具有使用者名稱 TestUser 和密碼密碼。</span><span class="sxs-lookup"><span data-stu-id="59327-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="59327-119">參數</span><span class="sxs-lookup"><span data-stu-id="59327-119">PARAMETERS</span></span>

### <span data-ttu-id="59327-120">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="59327-120">-BatchContext</span></span>
<span data-ttu-id="59327-121">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="59327-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="59327-122">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="59327-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="59327-123">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="59327-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="59327-124">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="59327-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="59327-125">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="59327-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59327-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="59327-126">-ComputeNode</span></span>
<span data-ttu-id="59327-127">指定計算節點作為 **PSComputeNode** 物件，此 Cmdlet 會在此物件上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="59327-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59327-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="59327-128">-ComputeNodeId</span></span>
<span data-ttu-id="59327-129">指定此 Cmdlet 建立使用者帳戶之計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="59327-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59327-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59327-130">-DefaultProfile</span></span>
<span data-ttu-id="59327-131">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="59327-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59327-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="59327-132">-ExpiryTime</span></span>
<span data-ttu-id="59327-133">指定新使用者帳戶的到期時間。</span><span class="sxs-lookup"><span data-stu-id="59327-133">Specifies the expiry time for the new user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59327-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="59327-134">-IsAdmin</span></span>
<span data-ttu-id="59327-135">表示 Cmdlet 會建立具有系統管理認證之使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="59327-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="59327-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="59327-136">-Name</span></span>
<span data-ttu-id="59327-137">指定新本地 Windows 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="59327-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59327-138">-密碼</span><span class="sxs-lookup"><span data-stu-id="59327-138">-Password</span></span>
<span data-ttu-id="59327-139">指定使用者帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="59327-139">Specifies the user account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59327-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="59327-140">-PoolId</span></span>
<span data-ttu-id="59327-141">指定包含要建立使用者帳戶之計算節點之資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="59327-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59327-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59327-142">CommonParameters</span></span>
<span data-ttu-id="59327-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="59327-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59327-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59327-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59327-145">輸入</span><span class="sxs-lookup"><span data-stu-id="59327-145">INPUTS</span></span>

### <span data-ttu-id="59327-146">Microsoft.Azure.Commands.Batch。Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="59327-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="59327-147">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="59327-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="59327-148">輸出</span><span class="sxs-lookup"><span data-stu-id="59327-148">OUTPUTS</span></span>

### <span data-ttu-id="59327-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="59327-149">System.Void</span></span>

## <span data-ttu-id="59327-150">筆記</span><span class="sxs-lookup"><span data-stu-id="59327-150">NOTES</span></span>

## <span data-ttu-id="59327-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="59327-151">RELATED LINKS</span></span>

[<span data-ttu-id="59327-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="59327-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="59327-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="59327-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="59327-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="59327-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="59327-155">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="59327-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
