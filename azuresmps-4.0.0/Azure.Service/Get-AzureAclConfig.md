---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0A32348E-C38D-4555-8F7C-6515F4EE7F23
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc1c469d35f4cc281fa22252e7e81509be06761
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967119"
---
# <span data-ttu-id="a34ac-101">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a34ac-101">Get-AzureAclConfig</span></span>

## <span data-ttu-id="a34ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a34ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a34ac-103">從 Azure 虛擬機器取得 ACL 設定物件。</span><span class="sxs-lookup"><span data-stu-id="a34ac-103">Gets the ACL configuration object from an Azure virtual machine.</span></span>

## <span data-ttu-id="a34ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="a34ac-104">SYNTAX</span></span>

```
Get-AzureAclConfig [[-EndpointName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a34ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="a34ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a34ac-106">**AzureAclConfig** Cmdlet 會從現有的 Azure 虛擬機器中取得存取控制清單 (ACL) 設定物件。</span><span class="sxs-lookup"><span data-stu-id="a34ac-106">The **Get-AzureAclConfig** cmdlet gets the access control list (ACL) configuration object from an existing Azure virtual machine.</span></span>

## <span data-ttu-id="a34ac-107">示例</span><span class="sxs-lookup"><span data-stu-id="a34ac-107">EXAMPLES</span></span>

### <span data-ttu-id="a34ac-108">範例1：取得虛擬機器端點的 ACL 設定物件</span><span class="sxs-lookup"><span data-stu-id="a34ac-108">Example 1: Get an ACL configuration object for a virtual machine endpoint</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
```

<span data-ttu-id="a34ac-109">第一個命令會透過使用 **xxxxx Cmdlet，** 在名為 ContosoService 的服務中，取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a34ac-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="a34ac-110">命令會使用管線運算子，將該物件傳遞到 **AzureAclConfig** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a34ac-110">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a34ac-111">該 Cmdlet 會取得名為 [Web] 的端點的 ACL 設定。</span><span class="sxs-lookup"><span data-stu-id="a34ac-111">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="a34ac-112">該命令會將該 ACL 設定物件儲存在 $Acl 變數中。</span><span class="sxs-lookup"><span data-stu-id="a34ac-112">The command stores that ACL configuration object in the $Acl variable.</span></span>

## <span data-ttu-id="a34ac-113">參數</span><span class="sxs-lookup"><span data-stu-id="a34ac-113">PARAMETERS</span></span>

### <span data-ttu-id="a34ac-114">-終結點</span><span class="sxs-lookup"><span data-stu-id="a34ac-114">-EndpointName</span></span>
<span data-ttu-id="a34ac-115">指定此 Cmdlet 取得其 ACL 的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="a34ac-115">Specifies the name of the endpoint for which this cmdlet gets an ACL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a34ac-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a34ac-116">-InformationAction</span></span>
<span data-ttu-id="a34ac-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="a34ac-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a34ac-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a34ac-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a34ac-119">持續</span><span class="sxs-lookup"><span data-stu-id="a34ac-119">Continue</span></span>
- <span data-ttu-id="a34ac-120">理會</span><span class="sxs-lookup"><span data-stu-id="a34ac-120">Ignore</span></span>
- <span data-ttu-id="a34ac-121">看</span><span class="sxs-lookup"><span data-stu-id="a34ac-121">Inquire</span></span>
- <span data-ttu-id="a34ac-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a34ac-122">SilentlyContinue</span></span>
- <span data-ttu-id="a34ac-123">停止</span><span class="sxs-lookup"><span data-stu-id="a34ac-123">Stop</span></span>
- <span data-ttu-id="a34ac-124">封存</span><span class="sxs-lookup"><span data-stu-id="a34ac-124">Suspend</span></span>

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

### <span data-ttu-id="a34ac-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a34ac-125">-InformationVariable</span></span>
<span data-ttu-id="a34ac-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="a34ac-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a34ac-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a34ac-127">-Profile</span></span>
<span data-ttu-id="a34ac-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a34ac-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a34ac-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a34ac-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a34ac-130">-VM</span><span class="sxs-lookup"><span data-stu-id="a34ac-130">-VM</span></span>
<span data-ttu-id="a34ac-131">指定此 Cmdlet 取得 ACL 設定的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="a34ac-131">Specifies the virtual machine object for which this cmdlet gets ACL configuration.</span></span>

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

### <span data-ttu-id="a34ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a34ac-132">CommonParameters</span></span>
<span data-ttu-id="a34ac-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a34ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a34ac-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a34ac-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a34ac-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a34ac-135">INPUTS</span></span>

## <span data-ttu-id="a34ac-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a34ac-136">OUTPUTS</span></span>

## <span data-ttu-id="a34ac-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a34ac-137">NOTES</span></span>

## <span data-ttu-id="a34ac-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a34ac-138">RELATED LINKS</span></span>

[<span data-ttu-id="a34ac-139">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a34ac-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a34ac-140">新-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a34ac-140">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="a34ac-141">移除-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a34ac-141">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="a34ac-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a34ac-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


