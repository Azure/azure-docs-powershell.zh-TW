---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 05a4b2a475b2bd58de706ba038f2760d133b7dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450181"
---
# <span data-ttu-id="07e34-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="07e34-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="07e34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07e34-102">SYNOPSIS</span></span>
<span data-ttu-id="07e34-103">移除端點和中繼資料以連接至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="07e34-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07e34-104">句法</span><span class="sxs-lookup"><span data-stu-id="07e34-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07e34-105">說明</span><span class="sxs-lookup"><span data-stu-id="07e34-105">DESCRIPTION</span></span>
<span data-ttu-id="07e34-106">Remove-AzureRmEnvironment Cmdlet 會移除端點和中繼資料資訊以連線至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="07e34-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="07e34-107">示例</span><span class="sxs-lookup"><span data-stu-id="07e34-107">EXAMPLES</span></span>

### <span data-ttu-id="07e34-108">範例1：建立及移除測試環境</span><span class="sxs-lookup"><span data-stu-id="07e34-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="07e34-109">這個範例示範如何使用 [載入 AzureRmEnvironment] 建立環境，然後如何使用 [移除] AzureRmEnvironment 刪除環境。</span><span class="sxs-lookup"><span data-stu-id="07e34-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="07e34-110">參數</span><span class="sxs-lookup"><span data-stu-id="07e34-110">PARAMETERS</span></span>

### <span data-ttu-id="07e34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e34-111">-DefaultProfile</span></span>
<span data-ttu-id="07e34-112">用於與 azure 進行通訊的認證、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="07e34-112">The credentials, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e34-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="07e34-113">-Name</span></span>
<span data-ttu-id="07e34-114">指定要移除的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="07e34-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="07e34-115">-範圍</span><span class="sxs-lookup"><span data-stu-id="07e34-115">-Scope</span></span>
<span data-ttu-id="07e34-116">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="07e34-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="07e34-117">-確認</span><span class="sxs-lookup"><span data-stu-id="07e34-117">-Confirm</span></span>
<span data-ttu-id="07e34-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="07e34-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07e34-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07e34-119">-WhatIf</span></span>
<span data-ttu-id="07e34-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07e34-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07e34-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07e34-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07e34-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e34-122">CommonParameters</span></span>
<span data-ttu-id="07e34-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07e34-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e34-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07e34-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e34-125">輸入</span><span class="sxs-lookup"><span data-stu-id="07e34-125">INPUTS</span></span>

### <span data-ttu-id="07e34-126">System.object</span><span class="sxs-lookup"><span data-stu-id="07e34-126">System.String</span></span>

## <span data-ttu-id="07e34-127">輸出</span><span class="sxs-lookup"><span data-stu-id="07e34-127">OUTPUTS</span></span>

### <span data-ttu-id="07e34-128">PSAzureEnvironment 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="07e34-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="07e34-129">筆記</span><span class="sxs-lookup"><span data-stu-id="07e34-129">NOTES</span></span>

## <span data-ttu-id="07e34-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="07e34-130">RELATED LINKS</span></span>

[<span data-ttu-id="07e34-131">附加 AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="07e34-131">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="07e34-132">AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="07e34-132">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="07e34-133">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="07e34-133">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

