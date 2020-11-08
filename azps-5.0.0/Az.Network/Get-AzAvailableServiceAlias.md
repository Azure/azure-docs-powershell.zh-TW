---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: acf9d604a793d4631641a87b222260d8687807cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139579"
---
# <span data-ttu-id="b70fc-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="b70fc-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="b70fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b70fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b70fc-103">在區域中取得可用的服務別名。</span><span class="sxs-lookup"><span data-stu-id="b70fc-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="b70fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b70fc-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b70fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="b70fc-105">DESCRIPTION</span></span>
<span data-ttu-id="b70fc-106">**AzAvailableServiceAlias** Cmdlet 可讓您在提供的位置中，取得子網的所有可用服務別名。</span><span class="sxs-lookup"><span data-stu-id="b70fc-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="b70fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="b70fc-107">EXAMPLES</span></span>

### <span data-ttu-id="b70fc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b70fc-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="b70fc-109">參數</span><span class="sxs-lookup"><span data-stu-id="b70fc-109">PARAMETERS</span></span>

### <span data-ttu-id="b70fc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70fc-110">-DefaultProfile</span></span>
<span data-ttu-id="b70fc-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b70fc-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b70fc-112">-位置</span><span class="sxs-lookup"><span data-stu-id="b70fc-112">-Location</span></span>
<span data-ttu-id="b70fc-113">位置。</span><span class="sxs-lookup"><span data-stu-id="b70fc-113">The location.</span></span>

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

### <span data-ttu-id="b70fc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70fc-114">CommonParameters</span></span>
<span data-ttu-id="b70fc-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b70fc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70fc-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b70fc-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70fc-117">輸入</span><span class="sxs-lookup"><span data-stu-id="b70fc-117">INPUTS</span></span>

### <span data-ttu-id="b70fc-118">System.object</span><span class="sxs-lookup"><span data-stu-id="b70fc-118">System.String</span></span>

## <span data-ttu-id="b70fc-119">輸出</span><span class="sxs-lookup"><span data-stu-id="b70fc-119">OUTPUTS</span></span>

### <span data-ttu-id="b70fc-120">PsAvailableServiceAlias 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b70fc-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="b70fc-121">筆記</span><span class="sxs-lookup"><span data-stu-id="b70fc-121">NOTES</span></span>

## <span data-ttu-id="b70fc-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="b70fc-122">RELATED LINKS</span></span>