---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 5acba21e8daf1adaa83820d67c5955b27230c4ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902650"
---
# <span data-ttu-id="fac9b-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="fac9b-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="fac9b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fac9b-102">SYNOPSIS</span></span>
<span data-ttu-id="fac9b-103">移除連接特定 Azure 實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fac9b-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="fac9b-104">語法</span><span class="sxs-lookup"><span data-stu-id="fac9b-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fac9b-105">描述</span><span class="sxs-lookup"><span data-stu-id="fac9b-105">DESCRIPTION</span></span>
<span data-ttu-id="fac9b-106">Cmdlet Remove-AzEnvironment移除端點和中繼資料資訊，以連接到特定 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="fac9b-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="fac9b-107">例子</span><span class="sxs-lookup"><span data-stu-id="fac9b-107">EXAMPLES</span></span>

### <span data-ttu-id="fac9b-108">範例 1：建立和移除測試環境</span><span class="sxs-lookup"><span data-stu-id="fac9b-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="fac9b-109">此範例顯示如何使用 Add-AzEnvironment 建立環境，以及如何使用 Remove-AzEnvironment 刪除環境。</span><span class="sxs-lookup"><span data-stu-id="fac9b-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="fac9b-110">參數</span><span class="sxs-lookup"><span data-stu-id="fac9b-110">PARAMETERS</span></span>

### <span data-ttu-id="fac9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac9b-111">-DefaultProfile</span></span>
<span data-ttu-id="fac9b-112">用於與 azure 通訊的認證、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fac9b-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fac9b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="fac9b-113">-Name</span></span>
<span data-ttu-id="fac9b-114">指定要移除的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="fac9b-114">Specifies the name of the environment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fac9b-115">-範圍</span><span class="sxs-lookup"><span data-stu-id="fac9b-115">-Scope</span></span>
<span data-ttu-id="fac9b-116">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或適用于此使用者啟動的所有會話。</span><span class="sxs-lookup"><span data-stu-id="fac9b-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac9b-117">-確認</span><span class="sxs-lookup"><span data-stu-id="fac9b-117">-Confirm</span></span>
<span data-ttu-id="fac9b-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fac9b-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac9b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fac9b-119">-WhatIf</span></span>
<span data-ttu-id="fac9b-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fac9b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fac9b-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fac9b-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac9b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac9b-122">CommonParameters</span></span>
<span data-ttu-id="fac9b-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fac9b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac9b-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fac9b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac9b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="fac9b-125">INPUTS</span></span>

### <span data-ttu-id="fac9b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="fac9b-126">System.String</span></span>

## <span data-ttu-id="fac9b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="fac9b-127">OUTPUTS</span></span>

### <span data-ttu-id="fac9b-128">Microsoft.Azure.Commands.Profile.models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="fac9b-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="fac9b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="fac9b-129">NOTES</span></span>

## <span data-ttu-id="fac9b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="fac9b-130">RELATED LINKS</span></span>

[<span data-ttu-id="fac9b-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="fac9b-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="fac9b-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="fac9b-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="fac9b-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="fac9b-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

