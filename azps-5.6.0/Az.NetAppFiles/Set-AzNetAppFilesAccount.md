---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: c5b8059561b859bd4ea7698b2cb41c9eb9a50a51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905977"
---
# <span data-ttu-id="1c766-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1c766-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="1c766-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1c766-102">SYNOPSIS</span></span>
<span data-ttu-id="1c766-103">使用新的資料集 (ANF) 帳戶更新 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="1c766-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="1c766-104">刪除相關聯的活動目錄時很有用。</span><span class="sxs-lookup"><span data-stu-id="1c766-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="1c766-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c766-105">SYNTAX</span></span>

### <span data-ttu-id="1c766-106">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1c766-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c766-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="1c766-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c766-108">描述</span><span class="sxs-lookup"><span data-stu-id="1c766-108">DESCRIPTION</span></span>
<span data-ttu-id="1c766-109">**Set-AzNetAppFilesAccount** Cmdlet 會修改 ANF 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1c766-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="1c766-110">例子</span><span class="sxs-lookup"><span data-stu-id="1c766-110">EXAMPLES</span></span>

### <span data-ttu-id="1c766-111">範例 1：修改 ANF 帳戶</span><span class="sxs-lookup"><span data-stu-id="1c766-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="1c766-112">此命令會執行對所給帳戶的更新。</span><span class="sxs-lookup"><span data-stu-id="1c766-112">This command performs an update on the given account.</span></span> <span data-ttu-id="1c766-113">如果沒有 Active Directory，表示該目錄會從帳戶中移除。</span><span class="sxs-lookup"><span data-stu-id="1c766-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="1c766-114">參數</span><span class="sxs-lookup"><span data-stu-id="1c766-114">PARAMETERS</span></span>

### <span data-ttu-id="1c766-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="1c766-115">-ActiveDirectory</span></span>
<span data-ttu-id="1c766-116">代表使用中目錄的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="1c766-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c766-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c766-117">-DefaultProfile</span></span>
<span data-ttu-id="1c766-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c766-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c766-119">-位置</span><span class="sxs-lookup"><span data-stu-id="1c766-119">-Location</span></span>
<span data-ttu-id="1c766-120">資源的位置</span><span class="sxs-lookup"><span data-stu-id="1c766-120">The location of the resource</span></span>

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

### <span data-ttu-id="1c766-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c766-121">-Name</span></span>
<span data-ttu-id="1c766-122">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="1c766-122">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c766-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c766-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c766-124">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="1c766-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1c766-125">-標記</span><span class="sxs-lookup"><span data-stu-id="1c766-125">-Tag</span></span>
<span data-ttu-id="1c766-126">代表資源標記的雜湊表</span><span class="sxs-lookup"><span data-stu-id="1c766-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="1c766-127">-確認</span><span class="sxs-lookup"><span data-stu-id="1c766-127">-Confirm</span></span>
<span data-ttu-id="1c766-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1c766-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c766-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c766-129">-WhatIf</span></span>
<span data-ttu-id="1c766-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c766-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c766-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c766-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c766-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c766-132">CommonParameters</span></span>
<span data-ttu-id="1c766-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1c766-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c766-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c766-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c766-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1c766-135">INPUTS</span></span>

### <span data-ttu-id="1c766-136">沒有</span><span class="sxs-lookup"><span data-stu-id="1c766-136">None</span></span>

## <span data-ttu-id="1c766-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1c766-137">OUTPUTS</span></span>

### <span data-ttu-id="1c766-138">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1c766-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="1c766-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1c766-139">NOTES</span></span>

## <span data-ttu-id="1c766-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c766-140">RELATED LINKS</span></span>
