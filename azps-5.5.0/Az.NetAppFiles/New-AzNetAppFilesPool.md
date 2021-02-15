---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: e1ebab6e0b32c6358defee30512185868581b6e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131434"
---
# <span data-ttu-id="4b8e7-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="4b8e7-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="4b8e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8e7-103"> (ANF) 池建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="4b8e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b8e7-104">SYNTAX</span></span>

### <span data-ttu-id="4b8e7-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4b8e7-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b8e7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b8e7-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b8e7-107">說明</span><span class="sxs-lookup"><span data-stu-id="4b8e7-107">DESCRIPTION</span></span>
<span data-ttu-id="4b8e7-108">**新的-AzNetAppFilesPool** Cmdlet 會建立 ANF 池。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="4b8e7-109">示例</span><span class="sxs-lookup"><span data-stu-id="4b8e7-109">EXAMPLES</span></span>

### <span data-ttu-id="4b8e7-110">範例1：建立 ANF 池</span><span class="sxs-lookup"><span data-stu-id="4b8e7-110">Example 1: Create an ANF pool</span></span>
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

<span data-ttu-id="4b8e7-111">這個命令會在帳戶 "MyAnfAccount" 中建立新的 ANF 池 "MyAnfPool"。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="4b8e7-112">參數</span><span class="sxs-lookup"><span data-stu-id="4b8e7-112">PARAMETERS</span></span>

### <span data-ttu-id="4b8e7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4b8e7-113">-AccountName</span></span>
<span data-ttu-id="4b8e7-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="4b8e7-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="4b8e7-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="4b8e7-115">-AccountObject</span></span>
<span data-ttu-id="4b8e7-116">新的 pool 物件帳戶</span><span class="sxs-lookup"><span data-stu-id="4b8e7-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="4b8e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b8e7-117">-DefaultProfile</span></span>
<span data-ttu-id="4b8e7-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b8e7-119">-位置</span><span class="sxs-lookup"><span data-stu-id="4b8e7-119">-Location</span></span>
<span data-ttu-id="4b8e7-120">資源的位置</span><span class="sxs-lookup"><span data-stu-id="4b8e7-120">The location of the resource</span></span>

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

### <span data-ttu-id="4b8e7-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b8e7-121">-Name</span></span>
<span data-ttu-id="4b8e7-122">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="4b8e7-122">The name of the ANF pool</span></span>

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

### <span data-ttu-id="4b8e7-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="4b8e7-123">-PoolSize</span></span>
<span data-ttu-id="4b8e7-124">ANF 池的大小</span><span class="sxs-lookup"><span data-stu-id="4b8e7-124">The size of the ANF pool</span></span>

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

### <span data-ttu-id="4b8e7-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="4b8e7-125">-QosType</span></span>
<span data-ttu-id="4b8e7-126">池的 qos 類型。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-126">The qos type of the pool.</span></span> <span data-ttu-id="4b8e7-127">可能的值包括： [Auto]、"Manual"</span><span class="sxs-lookup"><span data-stu-id="4b8e7-127">Possible values include: 'Auto', 'Manual'</span></span>

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

### <span data-ttu-id="4b8e7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b8e7-128">-ResourceGroupName</span></span>
<span data-ttu-id="4b8e7-129">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="4b8e7-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="4b8e7-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="4b8e7-130">-ServiceLevel</span></span>
<span data-ttu-id="4b8e7-131">ANF 池的服務層級</span><span class="sxs-lookup"><span data-stu-id="4b8e7-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="4b8e7-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b8e7-132">-Tag</span></span>
<span data-ttu-id="4b8e7-133">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="4b8e7-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="4b8e7-134">-確認</span><span class="sxs-lookup"><span data-stu-id="4b8e7-134">-Confirm</span></span>
<span data-ttu-id="4b8e7-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b8e7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b8e7-136">-WhatIf</span></span>
<span data-ttu-id="4b8e7-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b8e7-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b8e7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8e7-139">CommonParameters</span></span>
<span data-ttu-id="4b8e7-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8e7-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8e7-142">輸入</span><span class="sxs-lookup"><span data-stu-id="4b8e7-142">INPUTS</span></span>

### <span data-ttu-id="4b8e7-143">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="4b8e7-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4b8e7-144">OUTPUTS</span></span>

### <span data-ttu-id="4b8e7-145">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="4b8e7-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="4b8e7-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4b8e7-146">NOTES</span></span>

## <span data-ttu-id="4b8e7-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b8e7-147">RELATED LINKS</span></span>
