---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 557cfcaefef1a85fe7ad0a8bd62f4ddbf0ecb6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447812"
---
# <span data-ttu-id="c7705-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="c7705-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="c7705-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7705-102">SYNOPSIS</span></span>
<span data-ttu-id="c7705-103">在 DevTest 實驗中取得實驗室的自動關閉原則。</span><span class="sxs-lookup"><span data-stu-id="c7705-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7705-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7705-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7705-105">說明</span><span class="sxs-lookup"><span data-stu-id="c7705-105">DESCRIPTION</span></span>
<span data-ttu-id="c7705-106">**AzureRmDtlAutoShutdownPolicy** Cmdlet 會取得 lab 的自動關閉原則，這可讓您在一天中的指定時間自動關閉實驗室中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c7705-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="c7705-107">此 Cmdlet 會傳回是否已啟用原則的狀態，以及您設定為自動關閉實驗室虛擬機器的時間。</span><span class="sxs-lookup"><span data-stu-id="c7705-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="c7705-108">示例</span><span class="sxs-lookup"><span data-stu-id="c7705-108">EXAMPLES</span></span>

## <span data-ttu-id="c7705-109">參數</span><span class="sxs-lookup"><span data-stu-id="c7705-109">PARAMETERS</span></span>

### <span data-ttu-id="c7705-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7705-110">-DefaultProfile</span></span>
<span data-ttu-id="c7705-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c7705-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7705-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="c7705-112">-LabName</span></span>
<span data-ttu-id="c7705-113">指定此 Cmdlet 取得自動關閉原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="c7705-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7705-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7705-114">-ResourceGroupName</span></span>
<span data-ttu-id="c7705-115">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7705-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7705-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7705-116">CommonParameters</span></span>
<span data-ttu-id="c7705-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7705-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7705-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7705-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7705-119">輸入</span><span class="sxs-lookup"><span data-stu-id="c7705-119">INPUTS</span></span>

### <span data-ttu-id="c7705-120">所有</span><span class="sxs-lookup"><span data-stu-id="c7705-120">None</span></span>
<span data-ttu-id="c7705-121">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c7705-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7705-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c7705-122">OUTPUTS</span></span>

### <span data-ttu-id="c7705-123">PSSchedule 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="c7705-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="c7705-124">這個 Cmdlet 會傳回排程，以指定實驗室的虛擬機器必須關閉的時間。</span><span class="sxs-lookup"><span data-stu-id="c7705-124">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="c7705-125">筆記</span><span class="sxs-lookup"><span data-stu-id="c7705-125">NOTES</span></span>

## <span data-ttu-id="c7705-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7705-126">RELATED LINKS</span></span>

[<span data-ttu-id="c7705-127">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="c7705-127">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


