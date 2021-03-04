---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: 30a569c16a2f3da135f77061e8ff5373c45b2598
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906034"
---
# <span data-ttu-id="ec14d-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ec14d-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="ec14d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ec14d-102">SYNOPSIS</span></span>
<span data-ttu-id="ec14d-103">在 ANF 資料 (中) Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="ec14d-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="ec14d-104">語法</span><span class="sxs-lookup"><span data-stu-id="ec14d-104">SYNTAX</span></span>

### <span data-ttu-id="ec14d-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ec14d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec14d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec14d-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec14d-107">描述</span><span class="sxs-lookup"><span data-stu-id="ec14d-107">DESCRIPTION</span></span>
<span data-ttu-id="ec14d-108">**New-AzNetAppFilesPool** Cmdlet 會建立 ANF 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ec14d-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="ec14d-109">例子</span><span class="sxs-lookup"><span data-stu-id="ec14d-109">EXAMPLES</span></span>

### <span data-ttu-id="ec14d-110">範例 1：建立 ANF 資料庫</span><span class="sxs-lookup"><span data-stu-id="ec14d-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium" -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="ec14d-111">此命令會建立帳戶 「MyAnfAccount」內的新 ANF 資料庫 「MyAnfPool」。</span><span class="sxs-lookup"><span data-stu-id="ec14d-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="ec14d-112">參數</span><span class="sxs-lookup"><span data-stu-id="ec14d-112">PARAMETERS</span></span>

### <span data-ttu-id="ec14d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ec14d-113">-AccountName</span></span>
<span data-ttu-id="ec14d-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="ec14d-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="ec14d-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ec14d-115">-AccountObject</span></span>
<span data-ttu-id="ec14d-116">新資料庫物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="ec14d-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="ec14d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec14d-117">-DefaultProfile</span></span>
<span data-ttu-id="ec14d-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec14d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec14d-119">-位置</span><span class="sxs-lookup"><span data-stu-id="ec14d-119">-Location</span></span>
<span data-ttu-id="ec14d-120">資源的位置</span><span class="sxs-lookup"><span data-stu-id="ec14d-120">The location of the resource</span></span>

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

### <span data-ttu-id="ec14d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec14d-121">-Name</span></span>
<span data-ttu-id="ec14d-122">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="ec14d-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec14d-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="ec14d-123">-PoolSize</span></span>
<span data-ttu-id="ec14d-124">ANF 資料庫的大小</span><span class="sxs-lookup"><span data-stu-id="ec14d-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec14d-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="ec14d-125">-QosType</span></span>
<span data-ttu-id="ec14d-126">這是資料庫的 qos 類型。</span><span class="sxs-lookup"><span data-stu-id="ec14d-126">The qos type of the pool.</span></span> <span data-ttu-id="ec14d-127">可能的值包括：'自動'，'手動'</span><span class="sxs-lookup"><span data-stu-id="ec14d-127">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Auto
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec14d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec14d-128">-ResourceGroupName</span></span>
<span data-ttu-id="ec14d-129">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="ec14d-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ec14d-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="ec14d-130">-ServiceLevel</span></span>
<span data-ttu-id="ec14d-131">ANF 資料庫的服務等級</span><span class="sxs-lookup"><span data-stu-id="ec14d-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="ec14d-132">-標記</span><span class="sxs-lookup"><span data-stu-id="ec14d-132">-Tag</span></span>
<span data-ttu-id="ec14d-133">代表資源標記的雜湊表</span><span class="sxs-lookup"><span data-stu-id="ec14d-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="ec14d-134">-確認</span><span class="sxs-lookup"><span data-stu-id="ec14d-134">-Confirm</span></span>
<span data-ttu-id="ec14d-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ec14d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec14d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec14d-136">-WhatIf</span></span>
<span data-ttu-id="ec14d-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec14d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec14d-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec14d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec14d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec14d-139">CommonParameters</span></span>
<span data-ttu-id="ec14d-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ec14d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec14d-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec14d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec14d-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ec14d-142">INPUTS</span></span>

### <span data-ttu-id="ec14d-143">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ec14d-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="ec14d-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ec14d-144">OUTPUTS</span></span>

### <span data-ttu-id="ec14d-145">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ec14d-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="ec14d-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ec14d-146">NOTES</span></span>

## <span data-ttu-id="ec14d-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec14d-147">RELATED LINKS</span></span>
