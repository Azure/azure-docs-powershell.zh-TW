---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: 50d0345fea26d233147ad8373ab3daae785d6715
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625186"
---
# <span data-ttu-id="0022e-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="0022e-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="0022e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0022e-102">SYNOPSIS</span></span>
<span data-ttu-id="0022e-103">在 DevTest Labs 中取得 lab 的自動啟動原則。</span><span class="sxs-lookup"><span data-stu-id="0022e-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0022e-104">句法</span><span class="sxs-lookup"><span data-stu-id="0022e-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0022e-105">說明</span><span class="sxs-lookup"><span data-stu-id="0022e-105">DESCRIPTION</span></span>
<span data-ttu-id="0022e-106">**AzureRmDtlAutoStartPolicy** Cmdlet 會取得 lab 的自動啟動原則，此原則會安排自動啟動的實驗室虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0022e-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="0022e-107">這個 Cmdlet 會傳回原則的啟用或停用狀態，以及一周的天數，以及一天的時間，以及您已設定為允許將實驗室虛擬機器自動啟動的時間。</span><span class="sxs-lookup"><span data-stu-id="0022e-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="0022e-108">示例</span><span class="sxs-lookup"><span data-stu-id="0022e-108">EXAMPLES</span></span>

## <span data-ttu-id="0022e-109">參數</span><span class="sxs-lookup"><span data-stu-id="0022e-109">PARAMETERS</span></span>

### <span data-ttu-id="0022e-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="0022e-110">-LabName</span></span>
<span data-ttu-id="0022e-111">指定此 Cmdlet 取得自動啟動原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="0022e-111">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="0022e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0022e-112">-ResourceGroupName</span></span>
<span data-ttu-id="0022e-113">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0022e-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="0022e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0022e-114">-DefaultProfile</span></span>
<span data-ttu-id="0022e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0022e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0022e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0022e-116">CommonParameters</span></span>
<span data-ttu-id="0022e-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0022e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0022e-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0022e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0022e-119">輸入</span><span class="sxs-lookup"><span data-stu-id="0022e-119">INPUTS</span></span>

## <span data-ttu-id="0022e-120">輸出</span><span class="sxs-lookup"><span data-stu-id="0022e-120">OUTPUTS</span></span>

### <span data-ttu-id="0022e-121">PSSchedule 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="0022e-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="0022e-122">這個 Cmdlet 會傳回排程，指定實驗室的虛擬機器必須何時啟動。</span><span class="sxs-lookup"><span data-stu-id="0022e-122">This cmdlet returns the schedule that specifies when the lab's virtual machines must be started.</span></span>

## <span data-ttu-id="0022e-123">筆記</span><span class="sxs-lookup"><span data-stu-id="0022e-123">NOTES</span></span>

## <span data-ttu-id="0022e-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="0022e-124">RELATED LINKS</span></span>

[<span data-ttu-id="0022e-125">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="0022e-125">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)


