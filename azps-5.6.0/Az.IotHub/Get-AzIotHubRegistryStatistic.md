---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 251692538dbd9c5db28718c5833c9a3d096d9503
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911021"
---
# <span data-ttu-id="f56d3-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="f56d3-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="f56d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f56d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f56d3-103">獲得 IotHub 的 RegistryStatistics。</span><span class="sxs-lookup"><span data-stu-id="f56d3-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="f56d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="f56d3-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f56d3-105">描述</span><span class="sxs-lookup"><span data-stu-id="f56d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f56d3-106">獲得 IotHub 的 RegistryStatistics。</span><span class="sxs-lookup"><span data-stu-id="f56d3-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="f56d3-107">這會提供 IotHub 中總計、啟用和停用裝置數量的資訊。</span><span class="sxs-lookup"><span data-stu-id="f56d3-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="f56d3-108">例子</span><span class="sxs-lookup"><span data-stu-id="f56d3-108">EXAMPLES</span></span>

### <span data-ttu-id="f56d3-109">範例 1 取得 RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="f56d3-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f56d3-110">為名為 "myiothub" 的 IotHub 獲得 RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="f56d3-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f56d3-111">參數</span><span class="sxs-lookup"><span data-stu-id="f56d3-111">PARAMETERS</span></span>

### <span data-ttu-id="f56d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f56d3-112">-DefaultProfile</span></span>
<span data-ttu-id="f56d3-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f56d3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f56d3-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="f56d3-114">-Name</span></span>
<span data-ttu-id="f56d3-115">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="f56d3-115">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f56d3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f56d3-116">-ResourceGroupName</span></span>
<span data-ttu-id="f56d3-117">資源組名</span><span class="sxs-lookup"><span data-stu-id="f56d3-117">Resource Group Name</span></span>

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

### <span data-ttu-id="f56d3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f56d3-118">CommonParameters</span></span>
<span data-ttu-id="f56d3-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f56d3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f56d3-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f56d3-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f56d3-121">輸入</span><span class="sxs-lookup"><span data-stu-id="f56d3-121">INPUTS</span></span>

### <span data-ttu-id="f56d3-122">System.String</span><span class="sxs-lookup"><span data-stu-id="f56d3-122">System.String</span></span>

## <span data-ttu-id="f56d3-123">輸出</span><span class="sxs-lookup"><span data-stu-id="f56d3-123">OUTPUTS</span></span>

### <span data-ttu-id="f56d3-124">Microsoft.Azure.Commands.management.IotHub.models.PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="f56d3-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="f56d3-125">筆記</span><span class="sxs-lookup"><span data-stu-id="f56d3-125">NOTES</span></span>

## <span data-ttu-id="f56d3-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="f56d3-126">RELATED LINKS</span></span>
