---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 1a04f128326c0b2259b81d6c58c4bc7b0113e9db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127722"
---
# <span data-ttu-id="74221-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="74221-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="74221-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74221-102">SYNOPSIS</span></span>
<span data-ttu-id="74221-103">取得 (ANF) 音量的 Azure NetApp 檔案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="74221-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="74221-104">句法</span><span class="sxs-lookup"><span data-stu-id="74221-104">SYNTAX</span></span>

### <span data-ttu-id="74221-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="74221-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74221-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74221-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74221-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74221-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74221-108">說明</span><span class="sxs-lookup"><span data-stu-id="74221-108">DESCRIPTION</span></span>
<span data-ttu-id="74221-109">**AzNetAppFilesVolume** Cmdlet 會取得 ANF 體積的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="74221-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="74221-110">示例</span><span class="sxs-lookup"><span data-stu-id="74221-110">EXAMPLES</span></span>

### <span data-ttu-id="74221-111">範例1：取得 ANF 的音量</span><span class="sxs-lookup"><span data-stu-id="74221-111">Example 1: Get an ANF volume</span></span>
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

<span data-ttu-id="74221-112">這個命令會從 [MyAnfPool] 池中取得名為 MyAnfVolume 的卷名。</span><span class="sxs-lookup"><span data-stu-id="74221-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="74221-113">參數</span><span class="sxs-lookup"><span data-stu-id="74221-113">PARAMETERS</span></span>

### <span data-ttu-id="74221-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="74221-114">-AccountName</span></span>
<span data-ttu-id="74221-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="74221-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="74221-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74221-116">-DefaultProfile</span></span>
<span data-ttu-id="74221-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74221-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74221-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="74221-118">-Name</span></span>
<span data-ttu-id="74221-119">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="74221-119">The name of the ANF volume</span></span>

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

### <span data-ttu-id="74221-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="74221-120">-PoolName</span></span>
<span data-ttu-id="74221-121">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="74221-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="74221-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="74221-122">-PoolObject</span></span>
<span data-ttu-id="74221-123">包含要傳回之卷的 pool 物件</span><span class="sxs-lookup"><span data-stu-id="74221-123">The pool object containing the volume to return</span></span>

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

### <span data-ttu-id="74221-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74221-124">-ResourceGroupName</span></span>
<span data-ttu-id="74221-125">ANF 體積中的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="74221-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="74221-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74221-126">-ResourceId</span></span>
<span data-ttu-id="74221-127">ANF 體積的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="74221-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="74221-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74221-128">CommonParameters</span></span>
<span data-ttu-id="74221-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74221-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74221-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="74221-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74221-131">輸入</span><span class="sxs-lookup"><span data-stu-id="74221-131">INPUTS</span></span>

### <span data-ttu-id="74221-132">System.object</span><span class="sxs-lookup"><span data-stu-id="74221-132">System.String</span></span>

### <span data-ttu-id="74221-133">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="74221-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="74221-134">輸出</span><span class="sxs-lookup"><span data-stu-id="74221-134">OUTPUTS</span></span>

### <span data-ttu-id="74221-135">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="74221-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="74221-136">筆記</span><span class="sxs-lookup"><span data-stu-id="74221-136">NOTES</span></span>

## <span data-ttu-id="74221-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="74221-137">RELATED LINKS</span></span>