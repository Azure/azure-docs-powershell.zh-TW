---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 834a7444cda059614a7aa8b96acf99ba9cacd336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906050"
---
# <span data-ttu-id="a2f50-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a2f50-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="a2f50-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2f50-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f50-103">從 ANF 卷 (Azure NetApp 檔案) 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a2f50-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="a2f50-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2f50-104">SYNTAX</span></span>

### <span data-ttu-id="a2f50-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a2f50-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2f50-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2f50-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2f50-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2f50-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2f50-108">描述</span><span class="sxs-lookup"><span data-stu-id="a2f50-108">DESCRIPTION</span></span>
<span data-ttu-id="a2f50-109">**Get-AzNetAppFilesVolume** Cmdlet 會取得 ANF 音量的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a2f50-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="a2f50-110">例子</span><span class="sxs-lookup"><span data-stu-id="a2f50-110">EXAMPLES</span></span>

### <span data-ttu-id="a2f50-111">範例 1：取得 ANF 音量</span><span class="sxs-lookup"><span data-stu-id="a2f50-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="a2f50-112">此命令會從 「MyAnfPool」的集中獲得名為 MyAnfVolume 的音量。</span><span class="sxs-lookup"><span data-stu-id="a2f50-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="a2f50-113">參數</span><span class="sxs-lookup"><span data-stu-id="a2f50-113">PARAMETERS</span></span>

### <span data-ttu-id="a2f50-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a2f50-114">-AccountName</span></span>
<span data-ttu-id="a2f50-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="a2f50-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="a2f50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f50-116">-DefaultProfile</span></span>
<span data-ttu-id="a2f50-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2f50-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2f50-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2f50-118">-Name</span></span>
<span data-ttu-id="a2f50-119">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="a2f50-119">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2f50-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a2f50-120">-PoolName</span></span>
<span data-ttu-id="a2f50-121">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="a2f50-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a2f50-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="a2f50-122">-PoolObject</span></span>
<span data-ttu-id="a2f50-123">包含要返回之大量之資料表物件</span><span class="sxs-lookup"><span data-stu-id="a2f50-123">The pool object containing the volume to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2f50-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2f50-124">-ResourceGroupName</span></span>
<span data-ttu-id="a2f50-125">ANF 音量的資源群組</span><span class="sxs-lookup"><span data-stu-id="a2f50-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="a2f50-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2f50-126">-ResourceId</span></span>
<span data-ttu-id="a2f50-127">ANF 音量的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a2f50-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="a2f50-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f50-128">CommonParameters</span></span>
<span data-ttu-id="a2f50-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2f50-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f50-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2f50-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f50-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a2f50-131">INPUTS</span></span>

### <span data-ttu-id="a2f50-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a2f50-132">System.String</span></span>

### <span data-ttu-id="a2f50-133">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a2f50-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="a2f50-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a2f50-134">OUTPUTS</span></span>

### <span data-ttu-id="a2f50-135">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a2f50-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a2f50-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a2f50-136">NOTES</span></span>

## <span data-ttu-id="a2f50-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2f50-137">RELATED LINKS</span></span>
