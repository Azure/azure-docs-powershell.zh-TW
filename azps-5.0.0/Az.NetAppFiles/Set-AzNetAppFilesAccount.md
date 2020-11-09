---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286607"
---
# <span data-ttu-id="0e8bd-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0e8bd-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="0e8bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8bd-103">使用新的資料集，更新 (ANF) 帳戶的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="0e8bd-104">對於刪除關聯的活動目錄很有用。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="0e8bd-105">句法</span><span class="sxs-lookup"><span data-stu-id="0e8bd-105">SYNTAX</span></span>

### <span data-ttu-id="0e8bd-106">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0e8bd-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8bd-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="0e8bd-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e8bd-108">說明</span><span class="sxs-lookup"><span data-stu-id="0e8bd-108">DESCRIPTION</span></span>
<span data-ttu-id="0e8bd-109">**AzNetAppFilesAccount** Cmdlet 會修改 ANF 帳戶。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="0e8bd-110">示例</span><span class="sxs-lookup"><span data-stu-id="0e8bd-110">EXAMPLES</span></span>

### <span data-ttu-id="0e8bd-111">範例1：修改 ANF 帳戶</span><span class="sxs-lookup"><span data-stu-id="0e8bd-111">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="0e8bd-112">這個命令會在指定的帳號上執行更新。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-112">This command performs an update on the given account.</span></span> <span data-ttu-id="0e8bd-113">沒有 active directory 表示它將從帳戶中移除。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="0e8bd-114">參數</span><span class="sxs-lookup"><span data-stu-id="0e8bd-114">PARAMETERS</span></span>

### <span data-ttu-id="0e8bd-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="0e8bd-115">-ActiveDirectory</span></span>
<span data-ttu-id="0e8bd-116">代表活動目錄的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="0e8bd-116">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="0e8bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8bd-117">-DefaultProfile</span></span>
<span data-ttu-id="0e8bd-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e8bd-119">-位置</span><span class="sxs-lookup"><span data-stu-id="0e8bd-119">-Location</span></span>
<span data-ttu-id="0e8bd-120">資源的位置</span><span class="sxs-lookup"><span data-stu-id="0e8bd-120">The location of the resource</span></span>

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

### <span data-ttu-id="0e8bd-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e8bd-121">-Name</span></span>
<span data-ttu-id="0e8bd-122">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="0e8bd-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="0e8bd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8bd-123">-ResourceGroupName</span></span>
<span data-ttu-id="0e8bd-124">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="0e8bd-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="0e8bd-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e8bd-125">-Tag</span></span>
<span data-ttu-id="0e8bd-126">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="0e8bd-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="0e8bd-127">-確認</span><span class="sxs-lookup"><span data-stu-id="0e8bd-127">-Confirm</span></span>
<span data-ttu-id="0e8bd-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e8bd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8bd-129">-WhatIf</span></span>
<span data-ttu-id="0e8bd-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8bd-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e8bd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8bd-132">CommonParameters</span></span>
<span data-ttu-id="0e8bd-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8bd-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8bd-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0e8bd-135">INPUTS</span></span>

### <span data-ttu-id="0e8bd-136">所有</span><span class="sxs-lookup"><span data-stu-id="0e8bd-136">None</span></span>

## <span data-ttu-id="0e8bd-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0e8bd-137">OUTPUTS</span></span>

### <span data-ttu-id="0e8bd-138">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="0e8bd-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="0e8bd-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0e8bd-139">NOTES</span></span>

## <span data-ttu-id="0e8bd-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e8bd-140">RELATED LINKS</span></span>
