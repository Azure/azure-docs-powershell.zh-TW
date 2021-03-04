---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 83dbf747e2ddcd001320ac746b7c505df73a8169
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906433"
---
# <span data-ttu-id="8a40f-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8a40f-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="8a40f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8a40f-102">SYNOPSIS</span></span>
<span data-ttu-id="8a40f-103">重新 (重新) 從 Azure 網站修復服務提供者收到的資訊。</span><span class="sxs-lookup"><span data-stu-id="8a40f-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="8a40f-104">語法</span><span class="sxs-lookup"><span data-stu-id="8a40f-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a40f-105">描述</span><span class="sxs-lookup"><span data-stu-id="8a40f-105">DESCRIPTION</span></span>
<span data-ttu-id="8a40f-106">**Update-AzRecoveryServicesAsrServicesProvider Cmdlet** 會更新從 Azure 網站修復服務提供者收到的資訊。</span><span class="sxs-lookup"><span data-stu-id="8a40f-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="8a40f-107">您可以使用此 Cmdlet 來觸發復原服務提供者所收到資訊的重新更新。</span><span class="sxs-lookup"><span data-stu-id="8a40f-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="8a40f-108">例子</span><span class="sxs-lookup"><span data-stu-id="8a40f-108">EXAMPLES</span></span>

### <span data-ttu-id="8a40f-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="8a40f-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="8a40f-110">啟動從指定的 ASR 服務提供者重新組織資訊的工作，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="8a40f-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8a40f-111">參數</span><span class="sxs-lookup"><span data-stu-id="8a40f-111">PARAMETERS</span></span>

### <span data-ttu-id="8a40f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a40f-112">-DefaultProfile</span></span>
<span data-ttu-id="8a40f-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a40f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8a40f-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a40f-114">-InputObject</span></span>
<span data-ttu-id="8a40f-115">指定 ASR 服務提供者物件，用於識別要更新資訊的伺服器， (更新。) </span><span class="sxs-lookup"><span data-stu-id="8a40f-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a40f-116">-確認</span><span class="sxs-lookup"><span data-stu-id="8a40f-116">-Confirm</span></span>
<span data-ttu-id="8a40f-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8a40f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a40f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a40f-118">-WhatIf</span></span>
<span data-ttu-id="8a40f-119">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a40f-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a40f-120">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a40f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a40f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a40f-121">CommonParameters</span></span>
<span data-ttu-id="8a40f-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8a40f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a40f-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a40f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a40f-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8a40f-124">INPUTS</span></span>

### <span data-ttu-id="8a40f-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8a40f-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="8a40f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="8a40f-126">OUTPUTS</span></span>

### <span data-ttu-id="8a40f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8a40f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8a40f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="8a40f-128">NOTES</span></span>

## <span data-ttu-id="8a40f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a40f-129">RELATED LINKS</span></span>

[<span data-ttu-id="8a40f-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8a40f-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="8a40f-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8a40f-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
