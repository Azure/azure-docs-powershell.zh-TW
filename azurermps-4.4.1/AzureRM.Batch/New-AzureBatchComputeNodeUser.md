---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6289aa916b4d03559fccb11ea0a8897f4b506b53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450033"
---
# <span data-ttu-id="9c999-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="9c999-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="9c999-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c999-102">SYNOPSIS</span></span>
<span data-ttu-id="9c999-103">在批次計算節點上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="9c999-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c999-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c999-104">SYNTAX</span></span>

### <span data-ttu-id="9c999-105">標識號</span><span class="sxs-lookup"><span data-stu-id="9c999-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c999-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="9c999-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c999-107">說明</span><span class="sxs-lookup"><span data-stu-id="9c999-107">DESCRIPTION</span></span>
<span data-ttu-id="9c999-108">**新的 AzureBatchComputeNodeUser** Cmdlet 會在 Azure Batch 計算節點上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="9c999-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="9c999-109">示例</span><span class="sxs-lookup"><span data-stu-id="9c999-109">EXAMPLES</span></span>

### <span data-ttu-id="9c999-110">範例1：建立擁有管理認證的使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="9c999-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="9c999-111">這個命令會在具有識別碼 ComputeNode01 的 [計算] 節點上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="9c999-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="9c999-112">節點位於 ID 為 MyPool01 的池中。</span><span class="sxs-lookup"><span data-stu-id="9c999-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="9c999-113">使用者名稱為 TestUser、密碼為 Password、帳戶在七天后到期，且帳戶具有管理認證。</span><span class="sxs-lookup"><span data-stu-id="9c999-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="9c999-114">範例2：使用管線在計算節點上建立使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="9c999-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="9c999-115">這個命令會使用 **AzureBatchComputeNode** Cmdlet 取得名為 ComputeNode01 的計算節點。</span><span class="sxs-lookup"><span data-stu-id="9c999-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="9c999-116">該節點位於 ID 為 MyPool01 的池中。</span><span class="sxs-lookup"><span data-stu-id="9c999-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="9c999-117">命令會使用管線運算子，將該計算節點傳到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c999-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9c999-118">此命令會建立一個使用者帳戶，並將使用者名稱 TestUserand 密碼密碼。</span><span class="sxs-lookup"><span data-stu-id="9c999-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="9c999-119">參數</span><span class="sxs-lookup"><span data-stu-id="9c999-119">PARAMETERS</span></span>

### <span data-ttu-id="9c999-120">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="9c999-120">-BatchContext</span></span>
<span data-ttu-id="9c999-121">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="9c999-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9c999-122">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c999-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="9c999-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="9c999-123">-ComputeNode</span></span>
<span data-ttu-id="9c999-124">將此 Cmdlet 建立使用者帳戶的計算節點指定為 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="9c999-124">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="9c999-125">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="9c999-125">-ComputeNodeId</span></span>
<span data-ttu-id="9c999-126">指定此 Cmdlet 建立使用者帳戶的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c999-126">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="9c999-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9c999-127">-ExpiryTime</span></span>
<span data-ttu-id="9c999-128">指定新使用者帳戶的到期時間。</span><span class="sxs-lookup"><span data-stu-id="9c999-128">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="9c999-129">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="9c999-129">-IsAdmin</span></span>
<span data-ttu-id="9c999-130">表示 Cmdlet 會建立擁有管理認證的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="9c999-130">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="9c999-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c999-131">-Name</span></span>
<span data-ttu-id="9c999-132">指定新的本機 Windows 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9c999-132">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="9c999-133">-Password</span><span class="sxs-lookup"><span data-stu-id="9c999-133">-Password</span></span>
<span data-ttu-id="9c999-134">指定使用者帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="9c999-134">Specifies the user account password.</span></span>

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

### <span data-ttu-id="9c999-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="9c999-135">-PoolId</span></span>
<span data-ttu-id="9c999-136">指定包含要在其上建立使用者帳戶之計算節點的 pool 的 ID。</span><span class="sxs-lookup"><span data-stu-id="9c999-136">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="9c999-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c999-137">-DefaultProfile</span></span>
<span data-ttu-id="9c999-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c999-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c999-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c999-139">CommonParameters</span></span>
<span data-ttu-id="9c999-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c999-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c999-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c999-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c999-142">輸入</span><span class="sxs-lookup"><span data-stu-id="9c999-142">INPUTS</span></span>

### <span data-ttu-id="9c999-143">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="9c999-143">BatchAccountContext</span></span>
<span data-ttu-id="9c999-144">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9c999-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="9c999-145">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="9c999-145">PSComputeNode</span></span>
<span data-ttu-id="9c999-146">形參 "ComputeNode" 接受管線中 "PSComputeNode" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9c999-146">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="9c999-147">輸出</span><span class="sxs-lookup"><span data-stu-id="9c999-147">OUTPUTS</span></span>

## <span data-ttu-id="9c999-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9c999-148">NOTES</span></span>

## <span data-ttu-id="9c999-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c999-149">RELATED LINKS</span></span>

[<span data-ttu-id="9c999-150">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9c999-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9c999-151">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9c999-151">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="9c999-152">移除-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="9c999-152">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="9c999-153">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c999-153">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


