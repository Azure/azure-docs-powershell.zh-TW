---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: a3e83b4c58a7de2a0c020bc156e78656a6fd75ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620711"
---
# <span data-ttu-id="a9551-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a9551-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="a9551-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9551-102">SYNOPSIS</span></span>
<span data-ttu-id="a9551-103">針對儲存空間帳戶停用 [高級威脅防護原則]。</span><span class="sxs-lookup"><span data-stu-id="a9551-103">Disables the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="a9551-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9551-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9551-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9551-105">DESCRIPTION</span></span>
<span data-ttu-id="a9551-106">此 `Disable-AzSecurityAdvancedThreatProtection` Cmdlet 會針對儲存帳戶停用威脅 protetion 原則。</span><span class="sxs-lookup"><span data-stu-id="a9551-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protetion policy for a storage account.</span></span>
<span data-ttu-id="a9551-107">若要使用這個 Cmdlet，請指定 *ResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="a9551-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="a9551-108">示例</span><span class="sxs-lookup"><span data-stu-id="a9551-108">EXAMPLES</span></span>

### <span data-ttu-id="a9551-109">範例1</span><span class="sxs-lookup"><span data-stu-id="a9551-109">Example 1</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="a9551-110">這個命令會停用 [資源識別碼] 的高級威脅防護原則 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` 。</span><span class="sxs-lookup"><span data-stu-id="a9551-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="a9551-111">參數</span><span class="sxs-lookup"><span data-stu-id="a9551-111">PARAMETERS</span></span>

### <span data-ttu-id="a9551-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9551-112">-DefaultProfile</span></span>
<span data-ttu-id="a9551-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9551-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9551-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9551-114">-ResourceId</span></span>
<span data-ttu-id="a9551-115">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9551-115">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9551-116">-確認</span><span class="sxs-lookup"><span data-stu-id="a9551-116">-Confirm</span></span>
<span data-ttu-id="a9551-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9551-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9551-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9551-118">-WhatIf</span></span>
<span data-ttu-id="a9551-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9551-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9551-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9551-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9551-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9551-121">CommonParameters</span></span>
<span data-ttu-id="a9551-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9551-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9551-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9551-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9551-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a9551-124">INPUTS</span></span>

### <span data-ttu-id="a9551-125">所有</span><span class="sxs-lookup"><span data-stu-id="a9551-125">None</span></span>

## <span data-ttu-id="a9551-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a9551-126">OUTPUTS</span></span>

### <span data-ttu-id="a9551-127">PSAdvancedThreatProtection 中的 AdvancedThreatProtection （Security..。</span><span class="sxs-lookup"><span data-stu-id="a9551-127">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="a9551-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a9551-128">NOTES</span></span>

## <span data-ttu-id="a9551-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9551-129">RELATED LINKS</span></span>
