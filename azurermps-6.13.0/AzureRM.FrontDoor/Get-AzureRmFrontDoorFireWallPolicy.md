---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 283bc1a14404c842da0ed99e43596984b1559299
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451159"
---
# <span data-ttu-id="e4717-101">Get-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="e4717-101">Get-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="e4717-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4717-102">SYNOPSIS</span></span>
<span data-ttu-id="e4717-103">取得 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="e4717-103">Get WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4717-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4717-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4717-105">說明</span><span class="sxs-lookup"><span data-stu-id="e4717-105">DESCRIPTION</span></span>
<span data-ttu-id="e4717-106">**AzureRmFrontDoorFireWallPolicy** CmdletGet 會在目前訂閱底下的資源群組中取得 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="e4717-106">The **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="e4717-107">示例</span><span class="sxs-lookup"><span data-stu-id="e4717-107">EXAMPLES</span></span>

### <span data-ttu-id="e4717-108">範例1：在 $resourceGroup 中取得稱為 $Name 的 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="e4717-108">Example 1: Get a WAF policy called $Name in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="e4717-109">在 $resourceGroup 中取得稱為 $Name 的 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="e4717-109">Get a WAF policy called $Name in $resourceGroup</span></span>

### <span data-ttu-id="e4717-110">範例2：取得 $resourceGroup 中的所有 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="e4717-110">Example 2: Get all WAF policy in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name1}
Name               : {Name1}
Type               :

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name2}
Name               : {Name2}
Type               :
```

<span data-ttu-id="e4717-111">取得 $resourceGroup 中的所有 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="e4717-111">Get all WAF policy in $resourceGroup</span></span>

## <span data-ttu-id="e4717-112">參數</span><span class="sxs-lookup"><span data-stu-id="e4717-112">PARAMETERS</span></span>

### <span data-ttu-id="e4717-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4717-113">-DefaultProfile</span></span>
<span data-ttu-id="e4717-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4717-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4717-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4717-115">-Name</span></span>
<span data-ttu-id="e4717-116">FireWallPolicy [名稱]。</span><span class="sxs-lookup"><span data-stu-id="e4717-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4717-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4717-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4717-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4717-118">The resource group name.</span></span>

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

### <span data-ttu-id="e4717-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4717-119">CommonParameters</span></span>
<span data-ttu-id="e4717-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4717-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4717-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4717-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4717-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e4717-122">INPUTS</span></span>

### <span data-ttu-id="e4717-123">System.object</span><span class="sxs-lookup"><span data-stu-id="e4717-123">System.String</span></span>

## <span data-ttu-id="e4717-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e4717-124">OUTPUTS</span></span>

### <span data-ttu-id="e4717-125">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="e4717-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="e4717-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e4717-126">NOTES</span></span>

## <span data-ttu-id="e4717-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4717-127">RELATED LINKS</span></span>

<span data-ttu-id="e4717-128">[新-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
[移除-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="e4717-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span></span>
