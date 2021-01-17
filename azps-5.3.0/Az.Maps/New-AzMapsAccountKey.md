---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: c115cd780750770e05bc55b1f70a7cfe33967fff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436979"
---
# <span data-ttu-id="c7003-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="c7003-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="c7003-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7003-102">SYNOPSIS</span></span>
<span data-ttu-id="c7003-103">重新生成帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="c7003-103">Regenerates an account key.</span></span>

## <span data-ttu-id="c7003-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7003-104">SYNTAX</span></span>

### <span data-ttu-id="c7003-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c7003-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7003-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7003-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7003-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7003-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7003-108">說明</span><span class="sxs-lookup"><span data-stu-id="c7003-108">DESCRIPTION</span></span>
<span data-ttu-id="c7003-109">New-AzMapsAccountKey Cmdlet 會針對 Azure Maps 帳戶重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="c7003-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="c7003-110">示例</span><span class="sxs-lookup"><span data-stu-id="c7003-110">EXAMPLES</span></span>

### <span data-ttu-id="c7003-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c7003-111">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="c7003-112">在 [資源群組 MyResourceGroup] 中重新產生帳戶我的帳戶的主要 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="c7003-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="c7003-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c7003-113">Example 2</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="c7003-114">針對指定的 Azure 地圖帳戶重新產生次要 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="c7003-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="c7003-115">參數</span><span class="sxs-lookup"><span data-stu-id="c7003-115">PARAMETERS</span></span>

### <span data-ttu-id="c7003-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7003-116">-DefaultProfile</span></span>
<span data-ttu-id="c7003-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7003-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7003-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7003-118">-InputObject</span></span>
<span data-ttu-id="c7003-119">從 AzMapsAccount 將 [地圖] 帳戶成管道。</span><span class="sxs-lookup"><span data-stu-id="c7003-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="c7003-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c7003-120">-KeyName</span></span>
<span data-ttu-id="c7003-121">地圖帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="c7003-121">Maps Account Key.</span></span>

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

### <span data-ttu-id="c7003-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7003-122">-Name</span></span>
<span data-ttu-id="c7003-123">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c7003-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="c7003-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7003-124">-ResourceGroupName</span></span>
<span data-ttu-id="c7003-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c7003-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7003-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7003-126">-ResourceId</span></span>
<span data-ttu-id="c7003-127">地圖帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="c7003-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="c7003-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c7003-128">-Confirm</span></span>
<span data-ttu-id="c7003-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7003-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7003-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7003-130">-WhatIf</span></span>
<span data-ttu-id="c7003-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7003-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7003-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7003-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7003-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7003-133">CommonParameters</span></span>
<span data-ttu-id="c7003-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7003-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7003-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7003-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7003-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c7003-136">INPUTS</span></span>

### <span data-ttu-id="c7003-137">System.object</span><span class="sxs-lookup"><span data-stu-id="c7003-137">System.String</span></span>

### <span data-ttu-id="c7003-138">PSMapsAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c7003-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="c7003-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c7003-139">OUTPUTS</span></span>

### <span data-ttu-id="c7003-140">MapsAccountKeys 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="c7003-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="c7003-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c7003-141">NOTES</span></span>

## <span data-ttu-id="c7003-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7003-142">RELATED LINKS</span></span>
