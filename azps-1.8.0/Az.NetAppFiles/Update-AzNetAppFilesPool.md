---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 3dd02a2dc0cf7090ba2711b6155d25038397ab9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622205"
---
# <span data-ttu-id="d3332-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d3332-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="d3332-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3332-102">SYNOPSIS</span></span>
<span data-ttu-id="d3332-103">使用新的資料集，更新 (ANF) 池的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="d3332-103">Updates an Azure NetApp Files (ANF) pool with the new data set.</span></span>

## <span data-ttu-id="d3332-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3332-104">SYNTAX</span></span>

### <span data-ttu-id="d3332-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d3332-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3332-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3332-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String>
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3332-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3332-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -PoolSize <Int64> -ServiceLevel <String> -InputObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3332-108">說明</span><span class="sxs-lookup"><span data-stu-id="d3332-108">DESCRIPTION</span></span>
<span data-ttu-id="d3332-109">**AzNetAppFilesPool** Cmdlet 會修改 ANF 池。</span><span class="sxs-lookup"><span data-stu-id="d3332-109">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="d3332-110">示例</span><span class="sxs-lookup"><span data-stu-id="d3332-110">EXAMPLES</span></span>

### <span data-ttu-id="d3332-111">範例1：修改 ANF 池</span><span class="sxs-lookup"><span data-stu-id="d3332-111">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -ServiceLevel "Standard"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
ProvisioningState : Succeeded
```

<span data-ttu-id="d3332-112">這個命令會將 ANF 池子 "MyAnfPool" 變更為具有指定的大小和 ServiceLevel。</span><span class="sxs-lookup"><span data-stu-id="d3332-112">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="d3332-113">參數</span><span class="sxs-lookup"><span data-stu-id="d3332-113">PARAMETERS</span></span>

### <span data-ttu-id="d3332-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3332-114">-AccountName</span></span>
<span data-ttu-id="d3332-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="d3332-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3332-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="d3332-116">-AccountObject</span></span>
<span data-ttu-id="d3332-117">包含要更新之池的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="d3332-117">The account object containing the pool to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3332-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3332-118">-DefaultProfile</span></span>
<span data-ttu-id="d3332-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3332-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3332-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3332-120">-InputObject</span></span>
<span data-ttu-id="d3332-121">要更新的 pool 物件</span><span class="sxs-lookup"><span data-stu-id="d3332-121">The pool object to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3332-122">-位置</span><span class="sxs-lookup"><span data-stu-id="d3332-122">-Location</span></span>
<span data-ttu-id="d3332-123">資源的位置</span><span class="sxs-lookup"><span data-stu-id="d3332-123">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3332-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d3332-124">-Name</span></span>
<span data-ttu-id="d3332-125">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="d3332-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3332-126">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="d3332-126">-PoolSize</span></span>
<span data-ttu-id="d3332-127">ANF 池的大小</span><span class="sxs-lookup"><span data-stu-id="d3332-127">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3332-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3332-128">-ResourceGroupName</span></span>
<span data-ttu-id="d3332-129">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="d3332-129">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3332-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="d3332-130">-ServiceLevel</span></span>
<span data-ttu-id="d3332-131">ANF 池的服務層級</span><span class="sxs-lookup"><span data-stu-id="d3332-131">The service level of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3332-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d3332-132">-Confirm</span></span>
<span data-ttu-id="d3332-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3332-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3332-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3332-134">-WhatIf</span></span>
<span data-ttu-id="d3332-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3332-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3332-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3332-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3332-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3332-137">CommonParameters</span></span>
<span data-ttu-id="d3332-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3332-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d3332-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d3332-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3332-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d3332-140">INPUTS</span></span>

### <span data-ttu-id="d3332-141">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="d3332-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="d3332-142">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="d3332-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="d3332-143">輸出</span><span class="sxs-lookup"><span data-stu-id="d3332-143">OUTPUTS</span></span>

### <span data-ttu-id="d3332-144">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="d3332-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="d3332-145">筆記</span><span class="sxs-lookup"><span data-stu-id="d3332-145">NOTES</span></span>

## <span data-ttu-id="d3332-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3332-146">RELATED LINKS</span></span>
