---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: b65bfc61b354a5a45ac009b40b54de46d94ef56c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140578"
---
# <span data-ttu-id="021a9-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="021a9-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="021a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="021a9-102">SYNOPSIS</span></span>
<span data-ttu-id="021a9-103">取得 (ANF) 快照原則的 Azure NetApp 檔案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="021a9-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="021a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="021a9-104">SYNTAX</span></span>

### <span data-ttu-id="021a9-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="021a9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="021a9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="021a9-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="021a9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="021a9-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="021a9-108">說明</span><span class="sxs-lookup"><span data-stu-id="021a9-108">DESCRIPTION</span></span>
<span data-ttu-id="021a9-109">**AzNetAppFilesSnapshotPolicy** Cmdlet 會取得 ANF 快照原則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="021a9-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="021a9-110">示例</span><span class="sxs-lookup"><span data-stu-id="021a9-110">EXAMPLES</span></span>

### <span data-ttu-id="021a9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="021a9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="021a9-112">這個命令會取得帳戶「MyAnfAccount」的名為「MyBackupPolicy」的備份原則。</span><span class="sxs-lookup"><span data-stu-id="021a9-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="021a9-113">參數</span><span class="sxs-lookup"><span data-stu-id="021a9-113">PARAMETERS</span></span>

### <span data-ttu-id="021a9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="021a9-114">-AccountName</span></span>
<span data-ttu-id="021a9-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="021a9-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="021a9-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="021a9-116">-AccountObject</span></span>
<span data-ttu-id="021a9-117">新快照原則物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="021a9-117">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="021a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021a9-118">-DefaultProfile</span></span>
<span data-ttu-id="021a9-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="021a9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="021a9-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="021a9-120">-Name</span></span>
<span data-ttu-id="021a9-121">ANF 快照原則的名稱</span><span class="sxs-lookup"><span data-stu-id="021a9-121">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="021a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="021a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="021a9-123">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="021a9-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="021a9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="021a9-124">-ResourceId</span></span>
<span data-ttu-id="021a9-125">ANF 快照原則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="021a9-125">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="021a9-126">-確認</span><span class="sxs-lookup"><span data-stu-id="021a9-126">-Confirm</span></span>
<span data-ttu-id="021a9-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="021a9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="021a9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="021a9-128">-WhatIf</span></span>
<span data-ttu-id="021a9-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="021a9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="021a9-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="021a9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="021a9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021a9-131">CommonParameters</span></span>
<span data-ttu-id="021a9-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="021a9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021a9-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="021a9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021a9-134">輸入</span><span class="sxs-lookup"><span data-stu-id="021a9-134">INPUTS</span></span>

### <span data-ttu-id="021a9-135">System.object</span><span class="sxs-lookup"><span data-stu-id="021a9-135">System.String</span></span>

### <span data-ttu-id="021a9-136">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="021a9-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="021a9-137">輸出</span><span class="sxs-lookup"><span data-stu-id="021a9-137">OUTPUTS</span></span>

### <span data-ttu-id="021a9-138">PSNetAppFilesSnapshotPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="021a9-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="021a9-139">筆記</span><span class="sxs-lookup"><span data-stu-id="021a9-139">NOTES</span></span>

## <span data-ttu-id="021a9-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="021a9-140">RELATED LINKS</span></span>
