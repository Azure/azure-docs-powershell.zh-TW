---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: bea1f6d9427d0ed5dca48994d8138f954ed25ecd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796669"
---
# <span data-ttu-id="573d0-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="573d0-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="573d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="573d0-102">SYNOPSIS</span></span>
<span data-ttu-id="573d0-103">根據提供的選擇性修飾符，更新 (ANF) 池的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="573d0-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="573d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="573d0-104">SYNTAX</span></span>

### <span data-ttu-id="573d0-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="573d0-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="573d0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="573d0-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="573d0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="573d0-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="573d0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="573d0-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="573d0-109">說明</span><span class="sxs-lookup"><span data-stu-id="573d0-109">DESCRIPTION</span></span>
<span data-ttu-id="573d0-110">**AzNetAppFilesPool** Cmdlet 會修改 ANF 池。</span><span class="sxs-lookup"><span data-stu-id="573d0-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="573d0-111">示例</span><span class="sxs-lookup"><span data-stu-id="573d0-111">EXAMPLES</span></span>

### <span data-ttu-id="573d0-112">範例1：修改 ANF 池</span><span class="sxs-lookup"><span data-stu-id="573d0-112">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="573d0-113">這個命令會將 ANF 池子 "MyAnfPool" 變更為具有指定的大小和 ServiceLevel。</span><span class="sxs-lookup"><span data-stu-id="573d0-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="573d0-114">參數</span><span class="sxs-lookup"><span data-stu-id="573d0-114">PARAMETERS</span></span>

### <span data-ttu-id="573d0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="573d0-115">-AccountName</span></span>
<span data-ttu-id="573d0-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="573d0-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="573d0-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="573d0-117">-AccountObject</span></span>
<span data-ttu-id="573d0-118">包含要更新之池的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="573d0-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="573d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573d0-119">-DefaultProfile</span></span>
<span data-ttu-id="573d0-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="573d0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="573d0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="573d0-121">-InputObject</span></span>
<span data-ttu-id="573d0-122">要更新的 pool 物件</span><span class="sxs-lookup"><span data-stu-id="573d0-122">The pool object to update</span></span>

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

### <span data-ttu-id="573d0-123">-位置</span><span class="sxs-lookup"><span data-stu-id="573d0-123">-Location</span></span>
<span data-ttu-id="573d0-124">資源的位置</span><span class="sxs-lookup"><span data-stu-id="573d0-124">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573d0-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="573d0-125">-Name</span></span>
<span data-ttu-id="573d0-126">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="573d0-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="573d0-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="573d0-127">-PoolSize</span></span>
<span data-ttu-id="573d0-128">ANF 池的大小</span><span class="sxs-lookup"><span data-stu-id="573d0-128">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573d0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="573d0-129">-ResourceGroupName</span></span>
<span data-ttu-id="573d0-130">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="573d0-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="573d0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="573d0-131">-ResourceId</span></span>
<span data-ttu-id="573d0-132">ANF 池的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="573d0-132">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="573d0-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="573d0-133">-ServiceLevel</span></span>
<span data-ttu-id="573d0-134">ANF 池的服務層級</span><span class="sxs-lookup"><span data-stu-id="573d0-134">The service level of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573d0-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="573d0-135">-Tag</span></span>
<span data-ttu-id="573d0-136">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="573d0-136">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573d0-137">-確認</span><span class="sxs-lookup"><span data-stu-id="573d0-137">-Confirm</span></span>
<span data-ttu-id="573d0-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="573d0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="573d0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="573d0-139">-WhatIf</span></span>
<span data-ttu-id="573d0-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="573d0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="573d0-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="573d0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="573d0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573d0-142">CommonParameters</span></span>
<span data-ttu-id="573d0-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="573d0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="573d0-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="573d0-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573d0-145">輸入</span><span class="sxs-lookup"><span data-stu-id="573d0-145">INPUTS</span></span>

### <span data-ttu-id="573d0-146">System.object</span><span class="sxs-lookup"><span data-stu-id="573d0-146">System.String</span></span>

### <span data-ttu-id="573d0-147">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="573d0-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="573d0-148">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="573d0-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="573d0-149">輸出</span><span class="sxs-lookup"><span data-stu-id="573d0-149">OUTPUTS</span></span>

### <span data-ttu-id="573d0-150">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="573d0-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="573d0-151">筆記</span><span class="sxs-lookup"><span data-stu-id="573d0-151">NOTES</span></span>

## <span data-ttu-id="573d0-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="573d0-152">RELATED LINKS</span></span>
