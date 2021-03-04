---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 19f194d9402c2d5101b1da56c7c7a2a2208345aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906018"
---
# <span data-ttu-id="b865f-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b865f-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="b865f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b865f-102">SYNOPSIS</span></span>
<span data-ttu-id="b865f-103">刪除 ANF 帳戶 (Azure NetApp) 檔案。</span><span class="sxs-lookup"><span data-stu-id="b865f-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="b865f-104">語法</span><span class="sxs-lookup"><span data-stu-id="b865f-104">SYNTAX</span></span>

### <span data-ttu-id="b865f-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b865f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b865f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b865f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b865f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b865f-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b865f-108">描述</span><span class="sxs-lookup"><span data-stu-id="b865f-108">DESCRIPTION</span></span>
<span data-ttu-id="b865f-109">**Remove-AzNetAppFilesAccount** Cmdlet 會刪除 ANF 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b865f-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="b865f-110">例子</span><span class="sxs-lookup"><span data-stu-id="b865f-110">EXAMPLES</span></span>

### <span data-ttu-id="b865f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b865f-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="b865f-112">此命令會刪除 ANF 帳戶 「MyAnfAccount」。</span><span class="sxs-lookup"><span data-stu-id="b865f-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="b865f-113">參數</span><span class="sxs-lookup"><span data-stu-id="b865f-113">PARAMETERS</span></span>

### <span data-ttu-id="b865f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b865f-114">-DefaultProfile</span></span>
<span data-ttu-id="b865f-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b865f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b865f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b865f-116">-InputObject</span></span>
<span data-ttu-id="b865f-117">要移除的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="b865f-117">The account object to remove</span></span>

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

### <span data-ttu-id="b865f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b865f-118">-Name</span></span>
<span data-ttu-id="b865f-119">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="b865f-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b865f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b865f-120">-PassThru</span></span>
<span data-ttu-id="b865f-121">返回指定帳戶是否已成功移除</span><span class="sxs-lookup"><span data-stu-id="b865f-121">Return whether the specified account was successfully removed</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b865f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b865f-122">-ResourceGroupName</span></span>
<span data-ttu-id="b865f-123">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="b865f-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b865f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b865f-124">-ResourceId</span></span>
<span data-ttu-id="b865f-125">ANF 帳戶的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b865f-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="b865f-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b865f-126">-Confirm</span></span>
<span data-ttu-id="b865f-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b865f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b865f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b865f-128">-WhatIf</span></span>
<span data-ttu-id="b865f-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b865f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b865f-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b865f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b865f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b865f-131">CommonParameters</span></span>
<span data-ttu-id="b865f-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b865f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b865f-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b865f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b865f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b865f-134">INPUTS</span></span>

### <span data-ttu-id="b865f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b865f-135">System.String</span></span>

### <span data-ttu-id="b865f-136">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b865f-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="b865f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b865f-137">OUTPUTS</span></span>

### <span data-ttu-id="b865f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b865f-138">System.Boolean</span></span>

## <span data-ttu-id="b865f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b865f-139">NOTES</span></span>

## <span data-ttu-id="b865f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b865f-140">RELATED LINKS</span></span>
