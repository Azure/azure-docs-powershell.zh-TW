---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 915CBA29-5A58-4A5D-9F02-976CB76D4800
online version: ''
schema: 2.0.0
ms.openlocfilehash: af98cbdc0be73c87682d0ed004d17cd9e82c9baa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967621"
---
# <span data-ttu-id="686c0-101">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="686c0-101">Remove-AzureAclConfig</span></span>

## <span data-ttu-id="686c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="686c0-102">SYNOPSIS</span></span>
<span data-ttu-id="686c0-103">從 Azure 虛擬機器設定中移除 ACL 設定物件。</span><span class="sxs-lookup"><span data-stu-id="686c0-103">Removes an ACL configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="686c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="686c0-104">SYNTAX</span></span>

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="686c0-105">說明</span><span class="sxs-lookup"><span data-stu-id="686c0-105">DESCRIPTION</span></span>
<span data-ttu-id="686c0-106">**AzureAclConfig** Cmdlet 會從 Azure 虛擬機器設定中移除 (ACL) 設定物件的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="686c0-106">The **Remove-AzureAclConfig** cmdlet removes an access control list (ACL) configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="686c0-107">示例</span><span class="sxs-lookup"><span data-stu-id="686c0-107">EXAMPLES</span></span>

### <span data-ttu-id="686c0-108">範例1：移除 ACL 設定</span><span class="sxs-lookup"><span data-stu-id="686c0-108">Example 1: Remove an ACL configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

<span data-ttu-id="686c0-109">這個命令會透過使用 **VirtualMachine07 Cmdlet，** 在名為 ContosoService 的服務中，取得名為的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="686c0-109">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="686c0-110">命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="686c0-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="686c0-111">該 Cmdlet 會移除名為 [Web] 的端點的 ACL 設定。</span><span class="sxs-lookup"><span data-stu-id="686c0-111">That cmdlet removes the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="686c0-112">此命令會將結果傳遞到由 **updates Cmdlet （更新虛擬** 機）。</span><span class="sxs-lookup"><span data-stu-id="686c0-112">The command passes the result to the **Update-AzureVM** cmdlet, which updates the virtual machine.</span></span>

## <span data-ttu-id="686c0-113">參數</span><span class="sxs-lookup"><span data-stu-id="686c0-113">PARAMETERS</span></span>

### <span data-ttu-id="686c0-114">-終結點</span><span class="sxs-lookup"><span data-stu-id="686c0-114">-EndpointName</span></span>
<span data-ttu-id="686c0-115">指定此 Cmdlet 移除 ACL 設定的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="686c0-115">Specifies the name of the endpoint from which this cmdlet removes the ACL configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="686c0-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="686c0-116">-InformationAction</span></span>
<span data-ttu-id="686c0-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="686c0-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="686c0-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="686c0-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="686c0-119">持續</span><span class="sxs-lookup"><span data-stu-id="686c0-119">Continue</span></span>
- <span data-ttu-id="686c0-120">理會</span><span class="sxs-lookup"><span data-stu-id="686c0-120">Ignore</span></span>
- <span data-ttu-id="686c0-121">看</span><span class="sxs-lookup"><span data-stu-id="686c0-121">Inquire</span></span>
- <span data-ttu-id="686c0-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="686c0-122">SilentlyContinue</span></span>
- <span data-ttu-id="686c0-123">停止</span><span class="sxs-lookup"><span data-stu-id="686c0-123">Stop</span></span>
- <span data-ttu-id="686c0-124">封存</span><span class="sxs-lookup"><span data-stu-id="686c0-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="686c0-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="686c0-125">-InformationVariable</span></span>
<span data-ttu-id="686c0-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="686c0-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="686c0-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="686c0-127">-Profile</span></span>
<span data-ttu-id="686c0-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="686c0-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="686c0-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="686c0-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="686c0-130">-VM</span><span class="sxs-lookup"><span data-stu-id="686c0-130">-VM</span></span>
<span data-ttu-id="686c0-131">指定此 Cmdlet 移除 ACL 設定的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="686c0-131">Specifies the virtual machine from which this cmdlet removes an ACL configuration.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="686c0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="686c0-132">CommonParameters</span></span>
<span data-ttu-id="686c0-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="686c0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="686c0-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="686c0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="686c0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="686c0-135">INPUTS</span></span>

## <span data-ttu-id="686c0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="686c0-136">OUTPUTS</span></span>

## <span data-ttu-id="686c0-137">筆記</span><span class="sxs-lookup"><span data-stu-id="686c0-137">NOTES</span></span>

## <span data-ttu-id="686c0-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="686c0-138">RELATED LINKS</span></span>

[<span data-ttu-id="686c0-139">AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="686c0-139">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="686c0-140">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="686c0-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="686c0-141">新-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="686c0-141">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="686c0-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="686c0-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)

[<span data-ttu-id="686c0-143">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="686c0-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


