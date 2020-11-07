---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 4717fa187a8bd8234cd786ff5c6ad6d1678696b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625188"
---
# <span data-ttu-id="058e9-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="058e9-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="058e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="058e9-102">SYNOPSIS</span></span>
<span data-ttu-id="058e9-103">在 DevTest 實驗中取得實驗室的自動關閉原則。</span><span class="sxs-lookup"><span data-stu-id="058e9-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="058e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="058e9-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="058e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="058e9-105">DESCRIPTION</span></span>
<span data-ttu-id="058e9-106">**AzureRmDtlAutoShutdownPolicy** Cmdlet 會取得 lab 的自動關閉原則，這可讓您在一天中的指定時間自動關閉實驗室中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="058e9-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="058e9-107">此 Cmdlet 會傳回是否已啟用原則的狀態，以及您設定為自動關閉實驗室虛擬機器的時間。</span><span class="sxs-lookup"><span data-stu-id="058e9-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="058e9-108">示例</span><span class="sxs-lookup"><span data-stu-id="058e9-108">EXAMPLES</span></span>

## <span data-ttu-id="058e9-109">參數</span><span class="sxs-lookup"><span data-stu-id="058e9-109">PARAMETERS</span></span>

### <span data-ttu-id="058e9-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="058e9-110">-LabName</span></span>
<span data-ttu-id="058e9-111">指定此 Cmdlet 取得自動關閉原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="058e9-111">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="058e9-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="058e9-112">-ResourceGroupName</span></span>
<span data-ttu-id="058e9-113">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="058e9-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="058e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058e9-114">-DefaultProfile</span></span>
<span data-ttu-id="058e9-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="058e9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="058e9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058e9-116">CommonParameters</span></span>
<span data-ttu-id="058e9-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="058e9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="058e9-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="058e9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058e9-119">輸入</span><span class="sxs-lookup"><span data-stu-id="058e9-119">INPUTS</span></span>

## <span data-ttu-id="058e9-120">輸出</span><span class="sxs-lookup"><span data-stu-id="058e9-120">OUTPUTS</span></span>

### <span data-ttu-id="058e9-121">PSSchedule 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="058e9-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="058e9-122">這個 Cmdlet 會傳回排程，以指定實驗室的虛擬機器必須關閉的時間。</span><span class="sxs-lookup"><span data-stu-id="058e9-122">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="058e9-123">筆記</span><span class="sxs-lookup"><span data-stu-id="058e9-123">NOTES</span></span>

## <span data-ttu-id="058e9-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="058e9-124">RELATED LINKS</span></span>

[<span data-ttu-id="058e9-125">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="058e9-125">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


