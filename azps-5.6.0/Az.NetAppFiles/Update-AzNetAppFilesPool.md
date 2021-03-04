---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e8b367b724a4310eb5a3ed76bcf02e8538299845
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905950"
---
# <span data-ttu-id="ff360-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ff360-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="ff360-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ff360-102">SYNOPSIS</span></span>
<span data-ttu-id="ff360-103">根據提供的選擇性 (更新 ANF) 中的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="ff360-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="ff360-104">語法</span><span class="sxs-lookup"><span data-stu-id="ff360-104">SYNTAX</span></span>

### <span data-ttu-id="ff360-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ff360-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff360-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff360-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff360-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff360-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff360-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff360-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff360-109">描述</span><span class="sxs-lookup"><span data-stu-id="ff360-109">DESCRIPTION</span></span>
<span data-ttu-id="ff360-110">**Update-AzNetAppFilesPool** Cmdlet 會修改 ANF 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ff360-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="ff360-111">例子</span><span class="sxs-lookup"><span data-stu-id="ff360-111">EXAMPLES</span></span>

### <span data-ttu-id="ff360-112">範例 1：修改 ANF 資料庫</span><span class="sxs-lookup"><span data-stu-id="ff360-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="ff360-113">此命令將 ANF 資料庫 「MyAnfPool」變更為具有所給予的大小和 QosType。</span><span class="sxs-lookup"><span data-stu-id="ff360-113">This command changes the ANF pool "MyAnfPool" to have the given size and QosType.</span></span>

## <span data-ttu-id="ff360-114">參數</span><span class="sxs-lookup"><span data-stu-id="ff360-114">PARAMETERS</span></span>

### <span data-ttu-id="ff360-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff360-115">-AccountName</span></span>
<span data-ttu-id="ff360-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="ff360-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff360-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ff360-117">-AccountObject</span></span>
<span data-ttu-id="ff360-118">包含要更新之資料表的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ff360-118">The account object containing the pool to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff360-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff360-119">-DefaultProfile</span></span>
<span data-ttu-id="ff360-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff360-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff360-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff360-121">-InputObject</span></span>
<span data-ttu-id="ff360-122">要更新的集中物件</span><span class="sxs-lookup"><span data-stu-id="ff360-122">The pool object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff360-123">-位置</span><span class="sxs-lookup"><span data-stu-id="ff360-123">-Location</span></span>
<span data-ttu-id="ff360-124">資源的位置</span><span class="sxs-lookup"><span data-stu-id="ff360-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff360-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff360-125">-Name</span></span>
<span data-ttu-id="ff360-126">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="ff360-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff360-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="ff360-127">-PoolSize</span></span>
<span data-ttu-id="ff360-128">ANF 資料庫的大小</span><span class="sxs-lookup"><span data-stu-id="ff360-128">The size of the ANF pool</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff360-129">-QosType</span><span class="sxs-lookup"><span data-stu-id="ff360-129">-QosType</span></span>
<span data-ttu-id="ff360-130">這是資料庫的 qos 類型。</span><span class="sxs-lookup"><span data-stu-id="ff360-130">The qos type of the pool.</span></span> <span data-ttu-id="ff360-131">可能的值包括：'自動'，'手動'</span><span class="sxs-lookup"><span data-stu-id="ff360-131">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff360-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff360-132">-ResourceGroupName</span></span>
<span data-ttu-id="ff360-133">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="ff360-133">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff360-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff360-134">-ResourceId</span></span>
<span data-ttu-id="ff360-135">ANF 資料庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ff360-135">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff360-136">-標記</span><span class="sxs-lookup"><span data-stu-id="ff360-136">-Tag</span></span>
<span data-ttu-id="ff360-137">代表資源標記的雜湊表</span><span class="sxs-lookup"><span data-stu-id="ff360-137">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff360-138">-確認</span><span class="sxs-lookup"><span data-stu-id="ff360-138">-Confirm</span></span>
<span data-ttu-id="ff360-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ff360-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff360-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff360-140">-WhatIf</span></span>
<span data-ttu-id="ff360-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff360-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff360-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff360-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff360-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff360-143">CommonParameters</span></span>
<span data-ttu-id="ff360-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ff360-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff360-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff360-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff360-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ff360-146">INPUTS</span></span>

### <span data-ttu-id="ff360-147">System.String</span><span class="sxs-lookup"><span data-stu-id="ff360-147">System.String</span></span>

### <span data-ttu-id="ff360-148">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ff360-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="ff360-149">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ff360-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="ff360-150">輸出</span><span class="sxs-lookup"><span data-stu-id="ff360-150">OUTPUTS</span></span>

### <span data-ttu-id="ff360-151">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ff360-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="ff360-152">筆記</span><span class="sxs-lookup"><span data-stu-id="ff360-152">NOTES</span></span>

## <span data-ttu-id="ff360-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff360-153">RELATED LINKS</span></span>
