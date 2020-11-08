---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128684"
---
# <span data-ttu-id="bdfec-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="bdfec-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="bdfec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bdfec-102">SYNOPSIS</span></span>
<span data-ttu-id="bdfec-103">取得 IotHub 的 RegistryStatistics。</span><span class="sxs-lookup"><span data-stu-id="bdfec-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="bdfec-104">句法</span><span class="sxs-lookup"><span data-stu-id="bdfec-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdfec-105">說明</span><span class="sxs-lookup"><span data-stu-id="bdfec-105">DESCRIPTION</span></span>
<span data-ttu-id="bdfec-106">取得 IotHub 的 RegistryStatistics。</span><span class="sxs-lookup"><span data-stu-id="bdfec-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="bdfec-107">這會在 IotHub 中提供總數、啟用及停用裝置數目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bdfec-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="bdfec-108">示例</span><span class="sxs-lookup"><span data-stu-id="bdfec-108">EXAMPLES</span></span>

### <span data-ttu-id="bdfec-109">範例1取得 RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="bdfec-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="bdfec-110">取得名為 "myiothub" 的 IotHub 的 RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="bdfec-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="bdfec-111">參數</span><span class="sxs-lookup"><span data-stu-id="bdfec-111">PARAMETERS</span></span>

### <span data-ttu-id="bdfec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdfec-112">-DefaultProfile</span></span>
<span data-ttu-id="bdfec-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bdfec-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdfec-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="bdfec-114">-Name</span></span>
<span data-ttu-id="bdfec-115">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="bdfec-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="bdfec-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdfec-116">-ResourceGroupName</span></span>
<span data-ttu-id="bdfec-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="bdfec-117">Resource Group Name</span></span>

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

### <span data-ttu-id="bdfec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdfec-118">CommonParameters</span></span>
<span data-ttu-id="bdfec-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bdfec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdfec-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bdfec-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdfec-121">輸入</span><span class="sxs-lookup"><span data-stu-id="bdfec-121">INPUTS</span></span>

### <span data-ttu-id="bdfec-122">System.object</span><span class="sxs-lookup"><span data-stu-id="bdfec-122">System.String</span></span>

## <span data-ttu-id="bdfec-123">輸出</span><span class="sxs-lookup"><span data-stu-id="bdfec-123">OUTPUTS</span></span>

### <span data-ttu-id="bdfec-124">PSIotHubRegistryStatistics （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="bdfec-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="bdfec-125">筆記</span><span class="sxs-lookup"><span data-stu-id="bdfec-125">NOTES</span></span>

## <span data-ttu-id="bdfec-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdfec-126">RELATED LINKS</span></span>