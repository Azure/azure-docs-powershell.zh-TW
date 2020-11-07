---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 01b8283277c1d9592adbd8edfe6b883a4451ded9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624695"
---
# <span data-ttu-id="34280-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="34280-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="34280-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34280-102">SYNOPSIS</span></span>
<span data-ttu-id="34280-103">在目前的內容中設定預設值</span><span class="sxs-lookup"><span data-stu-id="34280-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34280-104">句法</span><span class="sxs-lookup"><span data-stu-id="34280-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34280-105">說明</span><span class="sxs-lookup"><span data-stu-id="34280-105">DESCRIPTION</span></span>
<span data-ttu-id="34280-106">Set-AzureRmDefault Cmdlet 會在目前的內容中新增或變更預設值。</span><span class="sxs-lookup"><span data-stu-id="34280-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="34280-107">示例</span><span class="sxs-lookup"><span data-stu-id="34280-107">EXAMPLES</span></span>

### <span data-ttu-id="34280-108">範例1</span><span class="sxs-lookup"><span data-stu-id="34280-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="34280-109">這個命令會將預設資源群組設定為使用者指定的資源群組。</span><span class="sxs-lookup"><span data-stu-id="34280-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="34280-110">參數</span><span class="sxs-lookup"><span data-stu-id="34280-110">PARAMETERS</span></span>

### <span data-ttu-id="34280-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34280-111">-DefaultProfile</span></span>
<span data-ttu-id="34280-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34280-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34280-113">-Force</span><span class="sxs-lookup"><span data-stu-id="34280-113">-Force</span></span>
<span data-ttu-id="34280-114">如果指定的預設值不存在，請建立新的資源群組</span><span class="sxs-lookup"><span data-stu-id="34280-114">Create a new resource group if specified default does not exist</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34280-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34280-115">-ResourceGroupName</span></span>
<span data-ttu-id="34280-116">設為預設值的資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="34280-116">Name of the resource group being set as default</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34280-117">-確認</span><span class="sxs-lookup"><span data-stu-id="34280-117">-Confirm</span></span>
<span data-ttu-id="34280-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="34280-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34280-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34280-119">-WhatIf</span></span>
<span data-ttu-id="34280-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="34280-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34280-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34280-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34280-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34280-122">CommonParameters</span></span>
<span data-ttu-id="34280-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34280-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34280-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="34280-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34280-125">輸入</span><span class="sxs-lookup"><span data-stu-id="34280-125">INPUTS</span></span>

### <span data-ttu-id="34280-126">System.object</span><span class="sxs-lookup"><span data-stu-id="34280-126">System.String</span></span>

## <span data-ttu-id="34280-127">輸出</span><span class="sxs-lookup"><span data-stu-id="34280-127">OUTPUTS</span></span>

### <span data-ttu-id="34280-128">[Internal .Resources. Resources]. 資源 ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="34280-128">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="34280-129">筆記</span><span class="sxs-lookup"><span data-stu-id="34280-129">NOTES</span></span>

## <span data-ttu-id="34280-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="34280-130">RELATED LINKS</span></span>

