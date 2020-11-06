---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
ms.openlocfilehash: 13364cde6799a6d99bcdba1d5cd2078c3392a2cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449755"
---
# <span data-ttu-id="ad5cc-101">New-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="ad5cc-101">New-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="ad5cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5cc-103">重新生成帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad5cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad5cc-104">SYNTAX</span></span>

### <span data-ttu-id="ad5cc-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ad5cc-105">NameParameterSet (Default)</span></span>
```
New-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad5cc-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad5cc-106">InputObjectParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad5cc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad5cc-107">ResourceIdParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad5cc-108">說明</span><span class="sxs-lookup"><span data-stu-id="ad5cc-108">DESCRIPTION</span></span>
<span data-ttu-id="ad5cc-109">New-AzureRmMapsAccountKey Cmdlet 會針對 Azure Maps 帳戶重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-109">The New-AzureRmMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="ad5cc-110">示例</span><span class="sxs-lookup"><span data-stu-id="ad5cc-110">EXAMPLES</span></span>

### <span data-ttu-id="ad5cc-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ad5cc-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="ad5cc-112">在 [資源群組 MyResourceGroup] 中重新產生帳戶我的帳戶的主要 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="ad5cc-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ad5cc-113">Example 2</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="ad5cc-114">針對指定的 Azure 地圖帳戶重新產生次要 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="ad5cc-115">參數</span><span class="sxs-lookup"><span data-stu-id="ad5cc-115">PARAMETERS</span></span>

### <span data-ttu-id="ad5cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5cc-116">-DefaultProfile</span></span>
<span data-ttu-id="ad5cc-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad5cc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad5cc-118">-InputObject</span></span>
<span data-ttu-id="ad5cc-119">從 AzureRmMapsAccount 將 [地圖] 帳戶成管道。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5cc-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ad5cc-120">-KeyName</span></span>
<span data-ttu-id="ad5cc-121">地圖帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5cc-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad5cc-122">-Name</span></span>
<span data-ttu-id="ad5cc-123">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad5cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad5cc-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5cc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad5cc-126">-ResourceId</span></span>
<span data-ttu-id="ad5cc-127">地圖帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5cc-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ad5cc-128">-Confirm</span></span>
<span data-ttu-id="ad5cc-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad5cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad5cc-130">-WhatIf</span></span>
<span data-ttu-id="ad5cc-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad5cc-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad5cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5cc-133">CommonParameters</span></span>
<span data-ttu-id="ad5cc-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5cc-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad5cc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5cc-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ad5cc-136">INPUTS</span></span>

### <span data-ttu-id="ad5cc-137">System.object</span><span class="sxs-lookup"><span data-stu-id="ad5cc-137">System.String</span></span>

### <span data-ttu-id="ad5cc-138">PSMapsAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ad5cc-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="ad5cc-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ad5cc-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ad5cc-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ad5cc-140">OUTPUTS</span></span>

### <span data-ttu-id="ad5cc-141">MapsAccountKeys 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="ad5cc-141">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="ad5cc-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ad5cc-142">NOTES</span></span>

## <span data-ttu-id="ad5cc-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad5cc-143">RELATED LINKS</span></span>
