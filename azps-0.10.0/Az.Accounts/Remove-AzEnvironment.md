---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: fa16d5f534a0bb26c0976cbc75700f7390f62466
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794121"
---
# <span data-ttu-id="3e86c-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3e86c-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="3e86c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e86c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e86c-103">移除端點和中繼資料以連接至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="3e86c-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="3e86c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e86c-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e86c-105">說明</span><span class="sxs-lookup"><span data-stu-id="3e86c-105">DESCRIPTION</span></span>
<span data-ttu-id="3e86c-106">Remove-AzEnvironment Cmdlet 會移除端點和中繼資料資訊以連線至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="3e86c-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="3e86c-107">示例</span><span class="sxs-lookup"><span data-stu-id="3e86c-107">EXAMPLES</span></span>

### <span data-ttu-id="3e86c-108">範例1：建立及移除測試環境</span><span class="sxs-lookup"><span data-stu-id="3e86c-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="3e86c-109">這個範例示範如何使用 [載入 AzEnvironment] 建立環境，然後如何使用 [移除] AzEnvironment 刪除環境。</span><span class="sxs-lookup"><span data-stu-id="3e86c-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="3e86c-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e86c-110">PARAMETERS</span></span>

### <span data-ttu-id="3e86c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e86c-111">-DefaultProfile</span></span>
<span data-ttu-id="3e86c-112">用於與 azure 進行通訊的認證、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e86c-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e86c-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e86c-113">-Name</span></span>
<span data-ttu-id="3e86c-114">指定要移除的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="3e86c-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="3e86c-115">-範圍</span><span class="sxs-lookup"><span data-stu-id="3e86c-115">-Scope</span></span>
<span data-ttu-id="3e86c-116">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="3e86c-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3e86c-117">-確認</span><span class="sxs-lookup"><span data-stu-id="3e86c-117">-Confirm</span></span>
<span data-ttu-id="3e86c-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e86c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e86c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e86c-119">-WhatIf</span></span>
<span data-ttu-id="3e86c-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e86c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e86c-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e86c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e86c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e86c-122">CommonParameters</span></span>
<span data-ttu-id="3e86c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e86c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e86c-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3e86c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e86c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="3e86c-125">INPUTS</span></span>

### <span data-ttu-id="3e86c-126">System.object</span><span class="sxs-lookup"><span data-stu-id="3e86c-126">System.String</span></span>

## <span data-ttu-id="3e86c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3e86c-127">OUTPUTS</span></span>

### <span data-ttu-id="3e86c-128">PSAzureEnvironment 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="3e86c-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="3e86c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="3e86c-129">NOTES</span></span>

## <span data-ttu-id="3e86c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e86c-130">RELATED LINKS</span></span>

[<span data-ttu-id="3e86c-131">附加 AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3e86c-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="3e86c-132">AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3e86c-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="3e86c-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3e86c-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)
