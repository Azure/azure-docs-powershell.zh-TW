---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: b742c8af0e8c36d07b2c608e74f0a02349502104
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622216"
---
# <span data-ttu-id="96947-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="96947-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="96947-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96947-102">SYNOPSIS</span></span>
<span data-ttu-id="96947-103"> (ANF) 卷中建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="96947-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="96947-104">句法</span><span class="sxs-lookup"><span data-stu-id="96947-104">SYNTAX</span></span>

### <span data-ttu-id="96947-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="96947-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96947-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96947-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96947-107">說明</span><span class="sxs-lookup"><span data-stu-id="96947-107">DESCRIPTION</span></span>
<span data-ttu-id="96947-108">**新的-AzNetAppFilesVolume** Cmdlet 會建立 ANF 的音量。</span><span class="sxs-lookup"><span data-stu-id="96947-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="96947-109">示例</span><span class="sxs-lookup"><span data-stu-id="96947-109">EXAMPLES</span></span>

### <span data-ttu-id="96947-110">範例1：建立 ANF 體積</span><span class="sxs-lookup"><span data-stu-id="96947-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="96947-111">這個命令會在「MyAnfPool」池中建立新的 ANF 音量「MyAnfVolume」。</span><span class="sxs-lookup"><span data-stu-id="96947-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="96947-112">參數</span><span class="sxs-lookup"><span data-stu-id="96947-112">PARAMETERS</span></span>

### <span data-ttu-id="96947-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="96947-113">-AccountName</span></span>
<span data-ttu-id="96947-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="96947-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="96947-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="96947-115">-CreationToken</span></span>
<span data-ttu-id="96947-116">卷的唯一檔路徑</span><span class="sxs-lookup"><span data-stu-id="96947-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="96947-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96947-117">-DefaultProfile</span></span>
<span data-ttu-id="96947-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96947-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96947-119">-位置</span><span class="sxs-lookup"><span data-stu-id="96947-119">-Location</span></span>
<span data-ttu-id="96947-120">資源的位置</span><span class="sxs-lookup"><span data-stu-id="96947-120">The location of the resource</span></span>

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

### <span data-ttu-id="96947-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="96947-121">-Name</span></span>
<span data-ttu-id="96947-122">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="96947-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96947-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="96947-123">-PoolName</span></span>
<span data-ttu-id="96947-124">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="96947-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="96947-125">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="96947-125">-PoolObject</span></span>
<span data-ttu-id="96947-126">新的 volume 物件集區</span><span class="sxs-lookup"><span data-stu-id="96947-126">The pool for the new volume object</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96947-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96947-127">-ResourceGroupName</span></span>
<span data-ttu-id="96947-128">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="96947-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="96947-129">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="96947-129">-ServiceLevel</span></span>
<span data-ttu-id="96947-130">ANF 容量的服務層級</span><span class="sxs-lookup"><span data-stu-id="96947-130">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="96947-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="96947-131">-SubnetId</span></span>
<span data-ttu-id="96947-132">委派子網的 Azure 資源 URI</span><span class="sxs-lookup"><span data-stu-id="96947-132">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="96947-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="96947-133">-Tag</span></span>
<span data-ttu-id="96947-134">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="96947-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="96947-135">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="96947-135">-UsageThreshold</span></span>
<span data-ttu-id="96947-136">檔案系統允許的儲存配額上限（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="96947-136">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="96947-137">-確認</span><span class="sxs-lookup"><span data-stu-id="96947-137">-Confirm</span></span>
<span data-ttu-id="96947-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="96947-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96947-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96947-139">-WhatIf</span></span>
<span data-ttu-id="96947-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96947-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96947-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96947-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96947-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96947-142">CommonParameters</span></span>
<span data-ttu-id="96947-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96947-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="96947-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96947-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96947-145">輸入</span><span class="sxs-lookup"><span data-stu-id="96947-145">INPUTS</span></span>

### <span data-ttu-id="96947-146">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="96947-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="96947-147">輸出</span><span class="sxs-lookup"><span data-stu-id="96947-147">OUTPUTS</span></span>

### <span data-ttu-id="96947-148">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="96947-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="96947-149">筆記</span><span class="sxs-lookup"><span data-stu-id="96947-149">NOTES</span></span>

## <span data-ttu-id="96947-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="96947-150">RELATED LINKS</span></span>
