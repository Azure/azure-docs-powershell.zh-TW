---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 2a31b5af374b1bc0f6136da61aa1c3672274e913
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905958"
---
# <span data-ttu-id="33bc8-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="33bc8-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="33bc8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="33bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="33bc8-103">根據提供的選擇性 (更新 anF) 帳戶的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="33bc8-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="33bc8-104">語法</span><span class="sxs-lookup"><span data-stu-id="33bc8-104">SYNTAX</span></span>

### <span data-ttu-id="33bc8-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="33bc8-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33bc8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33bc8-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33bc8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33bc8-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33bc8-108">描述</span><span class="sxs-lookup"><span data-stu-id="33bc8-108">DESCRIPTION</span></span>
<span data-ttu-id="33bc8-109">**Update-AzNetAppFilesAccount** Cmdlet 會修改 ANF 帳戶。</span><span class="sxs-lookup"><span data-stu-id="33bc8-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="33bc8-110">例子</span><span class="sxs-lookup"><span data-stu-id="33bc8-110">EXAMPLES</span></span>

### <span data-ttu-id="33bc8-111">範例 1：更新 ANF 帳戶</span><span class="sxs-lookup"><span data-stu-id="33bc8-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="33bc8-112">此命令會執行對所提供帳戶的更新，將標記修改為提供的帳戶。</span><span class="sxs-lookup"><span data-stu-id="33bc8-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="33bc8-113">參數</span><span class="sxs-lookup"><span data-stu-id="33bc8-113">PARAMETERS</span></span>

### <span data-ttu-id="33bc8-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="33bc8-114">-ActiveDirectory</span></span>
<span data-ttu-id="33bc8-115">代表使用中目錄的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="33bc8-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33bc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33bc8-116">-DefaultProfile</span></span>
<span data-ttu-id="33bc8-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="33bc8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33bc8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33bc8-118">-InputObject</span></span>
<span data-ttu-id="33bc8-119">要更新的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="33bc8-119">The account object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33bc8-120">-位置</span><span class="sxs-lookup"><span data-stu-id="33bc8-120">-Location</span></span>
<span data-ttu-id="33bc8-121">資源的位置</span><span class="sxs-lookup"><span data-stu-id="33bc8-121">The location of the resource</span></span>

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

### <span data-ttu-id="33bc8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="33bc8-122">-Name</span></span>
<span data-ttu-id="33bc8-123">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="33bc8-123">The name of the ANF account</span></span>

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

### <span data-ttu-id="33bc8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33bc8-124">-ResourceGroupName</span></span>
<span data-ttu-id="33bc8-125">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="33bc8-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="33bc8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33bc8-126">-ResourceId</span></span>
<span data-ttu-id="33bc8-127">ANF 帳戶的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="33bc8-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="33bc8-128">-標記</span><span class="sxs-lookup"><span data-stu-id="33bc8-128">-Tag</span></span>
<span data-ttu-id="33bc8-129">代表資源標記的雜湊表</span><span class="sxs-lookup"><span data-stu-id="33bc8-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="33bc8-130">-確認</span><span class="sxs-lookup"><span data-stu-id="33bc8-130">-Confirm</span></span>
<span data-ttu-id="33bc8-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="33bc8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33bc8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33bc8-132">-WhatIf</span></span>
<span data-ttu-id="33bc8-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33bc8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33bc8-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33bc8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33bc8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33bc8-135">CommonParameters</span></span>
<span data-ttu-id="33bc8-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="33bc8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33bc8-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33bc8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33bc8-138">輸入</span><span class="sxs-lookup"><span data-stu-id="33bc8-138">INPUTS</span></span>

### <span data-ttu-id="33bc8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="33bc8-139">System.String</span></span>

### <span data-ttu-id="33bc8-140">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="33bc8-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="33bc8-141">輸出</span><span class="sxs-lookup"><span data-stu-id="33bc8-141">OUTPUTS</span></span>

### <span data-ttu-id="33bc8-142">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="33bc8-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="33bc8-143">筆記</span><span class="sxs-lookup"><span data-stu-id="33bc8-143">NOTES</span></span>

## <span data-ttu-id="33bc8-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="33bc8-144">RELATED LINKS</span></span>
