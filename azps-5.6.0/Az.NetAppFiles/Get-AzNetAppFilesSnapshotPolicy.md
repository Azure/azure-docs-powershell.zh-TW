---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 3e93792a8698999599f67be84c3fe01e9c2ae508
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906066"
---
# <span data-ttu-id="273c2-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="273c2-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="273c2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="273c2-102">SYNOPSIS</span></span>
<span data-ttu-id="273c2-103">在快照策略中 (Azure NetApp 檔案) 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="273c2-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="273c2-104">語法</span><span class="sxs-lookup"><span data-stu-id="273c2-104">SYNTAX</span></span>

### <span data-ttu-id="273c2-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="273c2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="273c2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="273c2-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="273c2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="273c2-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="273c2-108">描述</span><span class="sxs-lookup"><span data-stu-id="273c2-108">DESCRIPTION</span></span>
<span data-ttu-id="273c2-109">**Get-AzNetAppFilessnapshotPolicy** Cmdlet 會取得 ANF 快照策略的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="273c2-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="273c2-110">例子</span><span class="sxs-lookup"><span data-stu-id="273c2-110">EXAMPLES</span></span>

### <span data-ttu-id="273c2-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="273c2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="273c2-112">此命令會針對帳戶 「MyAnfAccount」，獲得名為「MyBackupPolicy」的備份策略。</span><span class="sxs-lookup"><span data-stu-id="273c2-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="273c2-113">參數</span><span class="sxs-lookup"><span data-stu-id="273c2-113">PARAMETERS</span></span>

### <span data-ttu-id="273c2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="273c2-114">-AccountName</span></span>
<span data-ttu-id="273c2-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="273c2-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="273c2-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="273c2-116">-AccountObject</span></span>
<span data-ttu-id="273c2-117">新快照策略物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="273c2-117">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="273c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273c2-118">-DefaultProfile</span></span>
<span data-ttu-id="273c2-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="273c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="273c2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="273c2-120">-Name</span></span>
<span data-ttu-id="273c2-121">ANF 快照策略的名稱</span><span class="sxs-lookup"><span data-stu-id="273c2-121">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273c2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="273c2-122">-ResourceGroupName</span></span>
<span data-ttu-id="273c2-123">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="273c2-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="273c2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="273c2-124">-ResourceId</span></span>
<span data-ttu-id="273c2-125">ANF 快照策略的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="273c2-125">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="273c2-126">-確認</span><span class="sxs-lookup"><span data-stu-id="273c2-126">-Confirm</span></span>
<span data-ttu-id="273c2-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="273c2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="273c2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="273c2-128">-WhatIf</span></span>
<span data-ttu-id="273c2-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="273c2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="273c2-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="273c2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="273c2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273c2-131">CommonParameters</span></span>
<span data-ttu-id="273c2-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="273c2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273c2-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="273c2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273c2-134">輸入</span><span class="sxs-lookup"><span data-stu-id="273c2-134">INPUTS</span></span>

### <span data-ttu-id="273c2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="273c2-135">System.String</span></span>

### <span data-ttu-id="273c2-136">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="273c2-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="273c2-137">輸出</span><span class="sxs-lookup"><span data-stu-id="273c2-137">OUTPUTS</span></span>

### <span data-ttu-id="273c2-138">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilessnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="273c2-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="273c2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="273c2-139">NOTES</span></span>

## <span data-ttu-id="273c2-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="273c2-140">RELATED LINKS</span></span>
