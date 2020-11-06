---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 7116cd4c5da2dd897af4e6540593a5e5458e4eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448640"
---
# <span data-ttu-id="e59e5-101">New-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e59e5-101">New-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="e59e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e59e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e59e5-103">重新生成帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="e59e5-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e59e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="e59e5-104">SYNTAX</span></span>

### <span data-ttu-id="e59e5-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e59e5-105">NameParameterSet (Default)</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e59e5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e59e5-106">InputObjectParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e59e5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e59e5-107">ResourceIdParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e59e5-108">說明</span><span class="sxs-lookup"><span data-stu-id="e59e5-108">DESCRIPTION</span></span>
<span data-ttu-id="e59e5-109">**新的-AzureRmLocationBasedServicesAccountKey** Cmdlet 會為 [以位置為基礎的服務] 帳戶再生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e59e5-109">The **New-AzureRmLocationBasedServicesAccountKey** cmdlet regenerates an API key for a Location Based Services account.</span></span>

## <span data-ttu-id="e59e5-110">示例</span><span class="sxs-lookup"><span data-stu-id="e59e5-110">EXAMPLES</span></span>

### <span data-ttu-id="e59e5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e59e5-111">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="e59e5-112">在 [資源群組 MyResourceGroup] 中重新產生帳戶我的帳戶的主要 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e59e5-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="e59e5-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e59e5-113">Example 2</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="e59e5-114">針對指定的位置服務帳戶重新產生次要 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e59e5-114">Regenerates the Secondary API Key for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="e59e5-115">參數</span><span class="sxs-lookup"><span data-stu-id="e59e5-115">PARAMETERS</span></span>

### <span data-ttu-id="e59e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59e5-116">-DefaultProfile</span></span>
<span data-ttu-id="e59e5-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e59e5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e59e5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e59e5-118">-InputObject</span></span>
<span data-ttu-id="e59e5-119">[以位置為基礎的服務] 帳戶從 [AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md)中進行管道。</span><span class="sxs-lookup"><span data-stu-id="e59e5-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e59e5-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e59e5-120">-KeyName</span></span>
<span data-ttu-id="e59e5-121">[以位置為基礎的服務] 帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="e59e5-121">Location Based Services Account Key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e59e5-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e59e5-122">-Name</span></span>
<span data-ttu-id="e59e5-123">[以位置為基礎的服務] 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e59e5-123">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e59e5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e59e5-124">-ResourceGroupName</span></span>
<span data-ttu-id="e59e5-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e59e5-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e59e5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e59e5-126">-ResourceId</span></span>
<span data-ttu-id="e59e5-127">基於位置的服務帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="e59e5-127">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e59e5-128">-確認</span><span class="sxs-lookup"><span data-stu-id="e59e5-128">-Confirm</span></span>
<span data-ttu-id="e59e5-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e59e5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e59e5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e59e5-130">-WhatIf</span></span>
<span data-ttu-id="e59e5-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e59e5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e59e5-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e59e5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e59e5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59e5-133">CommonParameters</span></span>
<span data-ttu-id="e59e5-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e59e5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59e5-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e59e5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59e5-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e59e5-136">INPUTS</span></span>

### <span data-ttu-id="e59e5-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e59e5-137">System.String</span></span>
<span data-ttu-id="e59e5-138">LocationBasedServices. NewAzureLocationBasedServicesAccountKeyCommand + KeyNameType</span><span class="sxs-lookup"><span data-stu-id="e59e5-138">Microsoft.Azure.Commands.LocationBasedServices.NewAzureLocationBasedServicesAccountKeyCommand+KeyNameType</span></span>

## <span data-ttu-id="e59e5-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e59e5-139">OUTPUTS</span></span>

### <span data-ttu-id="e59e5-140">LocationBasedServicesAccountKeys 中的 LocationBasedServices。</span><span class="sxs-lookup"><span data-stu-id="e59e5-140">Microsoft.Azure.Management.LocationBasedServices.Models.LocationBasedServicesAccountKeys</span></span>

## <span data-ttu-id="e59e5-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e59e5-141">NOTES</span></span>

## <span data-ttu-id="e59e5-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e59e5-142">RELATED LINKS</span></span>
