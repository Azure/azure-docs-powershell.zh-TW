---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: 87d19475896138ee51a31694f707c1839f839ba8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904750"
---
# <span data-ttu-id="ec912-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ec912-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="ec912-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ec912-102">SYNOPSIS</span></span>
<span data-ttu-id="ec912-103">檢查組配置存放區名稱是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="ec912-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="ec912-104">語法</span><span class="sxs-lookup"><span data-stu-id="ec912-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec912-105">描述</span><span class="sxs-lookup"><span data-stu-id="ec912-105">DESCRIPTION</span></span>
<span data-ttu-id="ec912-106">檢查組配置存放區名稱是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="ec912-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="ec912-107">例子</span><span class="sxs-lookup"><span data-stu-id="ec912-107">EXAMPLES</span></span>

### <span data-ttu-id="ec912-108">範例 1：測試應用程式組配置存放區名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="ec912-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="ec912-109">此命令會測試應用程式組配置存放區名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="ec912-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="ec912-110">參數</span><span class="sxs-lookup"><span data-stu-id="ec912-110">PARAMETERS</span></span>

### <span data-ttu-id="ec912-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec912-111">-DefaultProfile</span></span>
<span data-ttu-id="ec912-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec912-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec912-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec912-113">-Name</span></span>
<span data-ttu-id="ec912-114">檢查可用性的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec912-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="ec912-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec912-115">-SubscriptionId</span></span>
<span data-ttu-id="ec912-116">Microsoft Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec912-116">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec912-117">-確認</span><span class="sxs-lookup"><span data-stu-id="ec912-117">-Confirm</span></span>
<span data-ttu-id="ec912-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ec912-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec912-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec912-119">-WhatIf</span></span>
<span data-ttu-id="ec912-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec912-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec912-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec912-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec912-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec912-122">CommonParameters</span></span>
<span data-ttu-id="ec912-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ec912-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec912-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec912-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec912-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ec912-125">INPUTS</span></span>

## <span data-ttu-id="ec912-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ec912-126">OUTPUTS</span></span>

### <span data-ttu-id="ec912-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="ec912-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="ec912-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ec912-128">NOTES</span></span>

<span data-ttu-id="ec912-129">別名</span><span class="sxs-lookup"><span data-stu-id="ec912-129">ALIASES</span></span>

## <span data-ttu-id="ec912-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec912-130">RELATED LINKS</span></span>

