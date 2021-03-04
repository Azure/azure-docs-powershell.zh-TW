---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: 4eb210380feaaf101bad45b4bd0b4df26533f9e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912737"
---
# <span data-ttu-id="40a93-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="40a93-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="40a93-102">簡介</span><span class="sxs-lookup"><span data-stu-id="40a93-102">SYNOPSIS</span></span>
<span data-ttu-id="40a93-103">取得地區中的可用服務別名。</span><span class="sxs-lookup"><span data-stu-id="40a93-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="40a93-104">語法</span><span class="sxs-lookup"><span data-stu-id="40a93-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40a93-105">描述</span><span class="sxs-lookup"><span data-stu-id="40a93-105">DESCRIPTION</span></span>
<span data-ttu-id="40a93-106">**Get-AzAvailableServiceAlias Cmdlet** 可讓您在提供的位置中，為子網取得所有可用的服務別名。</span><span class="sxs-lookup"><span data-stu-id="40a93-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="40a93-107">例子</span><span class="sxs-lookup"><span data-stu-id="40a93-107">EXAMPLES</span></span>

### <span data-ttu-id="40a93-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="40a93-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="40a93-109">參數</span><span class="sxs-lookup"><span data-stu-id="40a93-109">PARAMETERS</span></span>

### <span data-ttu-id="40a93-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40a93-110">-DefaultProfile</span></span>
<span data-ttu-id="40a93-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="40a93-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40a93-112">-位置</span><span class="sxs-lookup"><span data-stu-id="40a93-112">-Location</span></span>
<span data-ttu-id="40a93-113">位置。</span><span class="sxs-lookup"><span data-stu-id="40a93-113">The location.</span></span>

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

### <span data-ttu-id="40a93-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a93-114">CommonParameters</span></span>
<span data-ttu-id="40a93-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="40a93-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a93-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40a93-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a93-117">輸入</span><span class="sxs-lookup"><span data-stu-id="40a93-117">INPUTS</span></span>

### <span data-ttu-id="40a93-118">System.String</span><span class="sxs-lookup"><span data-stu-id="40a93-118">System.String</span></span>

## <span data-ttu-id="40a93-119">輸出</span><span class="sxs-lookup"><span data-stu-id="40a93-119">OUTPUTS</span></span>

### <span data-ttu-id="40a93-120">Microsoft.Azure.Commands.network.models.PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="40a93-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="40a93-121">筆記</span><span class="sxs-lookup"><span data-stu-id="40a93-121">NOTES</span></span>

## <span data-ttu-id="40a93-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="40a93-122">RELATED LINKS</span></span>
