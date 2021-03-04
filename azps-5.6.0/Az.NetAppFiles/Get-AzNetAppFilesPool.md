---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 546364e96f7beed16ae8786dc3aaacbf9a84454d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906077"
---
# <span data-ttu-id="b6e2d-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b6e2d-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="b6e2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b6e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e2d-103">在 ANF 資料庫或資料庫 (Azure NetApp 檔案) 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b6e2d-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="b6e2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="b6e2d-104">SYNTAX</span></span>

### <span data-ttu-id="b6e2d-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b6e2d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6e2d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6e2d-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6e2d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6e2d-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6e2d-108">描述</span><span class="sxs-lookup"><span data-stu-id="b6e2d-108">DESCRIPTION</span></span>
<span data-ttu-id="b6e2d-109">**Get-AzNetAppFilesPool** Cmdlet 會取得 ANF 資料庫的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b6e2d-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="b6e2d-110">例子</span><span class="sxs-lookup"><span data-stu-id="b6e2d-110">EXAMPLES</span></span>

### <span data-ttu-id="b6e2d-111">範例 1：取得 ANF 區</span><span class="sxs-lookup"><span data-stu-id="b6e2d-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

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

<span data-ttu-id="b6e2d-112">此命令會從「MyAnfAccount」帳戶獲得名為 MyAnfPool 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="b6e2d-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="b6e2d-113">參數</span><span class="sxs-lookup"><span data-stu-id="b6e2d-113">PARAMETERS</span></span>

### <span data-ttu-id="b6e2d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6e2d-114">-AccountName</span></span>
<span data-ttu-id="b6e2d-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="b6e2d-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="b6e2d-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b6e2d-116">-AccountObject</span></span>
<span data-ttu-id="b6e2d-117">包含要退回之資料表的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="b6e2d-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="b6e2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e2d-118">-DefaultProfile</span></span>
<span data-ttu-id="b6e2d-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6e2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6e2d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6e2d-120">-Name</span></span>
<span data-ttu-id="b6e2d-121">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="b6e2d-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="b6e2d-123">ANF 資料庫的資源群組</span><span class="sxs-lookup"><span data-stu-id="b6e2d-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="b6e2d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e2d-124">-ResourceId</span></span>
<span data-ttu-id="b6e2d-125">ANF 資料庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b6e2d-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="b6e2d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e2d-126">CommonParameters</span></span>
<span data-ttu-id="b6e2d-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b6e2d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e2d-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6e2d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e2d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b6e2d-129">INPUTS</span></span>

### <span data-ttu-id="b6e2d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b6e2d-130">System.String</span></span>

### <span data-ttu-id="b6e2d-131">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b6e2d-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="b6e2d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b6e2d-132">OUTPUTS</span></span>

### <span data-ttu-id="b6e2d-133">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b6e2d-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="b6e2d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b6e2d-134">NOTES</span></span>

## <span data-ttu-id="b6e2d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6e2d-135">RELATED LINKS</span></span>
